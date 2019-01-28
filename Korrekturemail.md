Hi mongoq,

One of my colleague faced with Quartus2 error with "tm1637_standalone.vhd" file:
...
Error (10346): VHDL error at tm1637_standalone.vhd(231): formal port or parameter "in_digit0" must have actual or default value
...
After he fixed line# 231it works OK.

Fix details:
 -> was:
 
      when 65 => scl <= '0'; sda <= int_to_seg7(display, 2, 2), reg_digit0, reg_digit1, reg_digit2, reg_digit3;
      
 -> now:
 
      when 65 => scl <= '0'; sda <= int_to_seg7(display, 2, 2, reg_digit0, reg_digit1, reg_digit2, reg_digit3);

I think you should know about this problem in your source code when assembling with Quartus2 software.

With best regards,
Igor K.

---

Kann ich jedoch nicht nachvollziehen. Die Funktion **int_to_seg7** hat vier Übergabeparameter ?!!! 

---

Hi Mark,

It was my mistake, there was no time to check original src in GitHub to verify exact status. Only after you point me to original src I've found that my colleague faced with problem during original code modification.
/ I am busy with network design now, so I am not following tasks that other group did - only consulting /

Regarding Quartus index - it came from the history : originally it was Quartus, that Altera announced Quartus2 and after Altera was acquired by Intel there was no  announcement about index change - so internally we call it "Q2".
My colleague used Quartus version 16 'Lite' edition to assemble his design.

Anyway, you described a problem but my colleague could not reproduce it with modified component. You can find modified code it attach:
-> tm1637_external_connect.vhd
My colleague told me that with this component they have no problem with output any 16bit value. New port interface:
    Port (    clk25     : in  std_logic;
                data     : std_logic_vector(15 downto 0); -- !!!
                scl   : out std_logic;
                sda   : out std_logic
          );
In global, this component could not provide ACK-kind signal when data uploaded into " tm1637" HW (to signal that new data can be written to DATA-port) to upper logic, so expecting problem in case when you will change values faster than it can be uploaded into HW.
So, to avoid problems with HW you must construct this ACK-kind signal and use it in upper logic.

Hope it will be useful for you.

With best regards,
Igor K.
