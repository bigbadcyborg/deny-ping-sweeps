# deny-ping-sweeps
disable ICMP echo requests to prevent ping sweeps on your ports.


#Linux:<br>
<br>Using sysctl:

            $sudo nano /etc/sysctl.conf

Add the following line then save:

            net.ipv4.icmp_echo_ignore_all = 1

Apply the changes:

            sudo sysctl -p

#Windows Powershell:<br>


            New-NetFirewallRule -DisplayName "Block ICMPv4" -Protocol ICMPv4 -Action Block


        
