
📄 README: Linux UFW Firewall Rule Configuration & Testing

Objective:
Configure and test basic firewall rules using UFW (Uncomplicated Firewall) in Linux to allow or block specific traffic.

Tools Used:
- UFW (pre-installed on many Linux systems)
- Telnet / Nmap for testing (install if not available)

Steps Performed:

1. Enable UFW (if not already enabled):
   sudo ufw enable

2. View current firewall rules:
   sudo ufw status numbered

3. Add rule to block port 23 (Telnet):
   sudo ufw deny 23

4. Verify the rule is added:
   sudo ufw status numbered

5. Test the rule using Telnet or Nmap:
   telnet localhost 23
   OR
   nmap -p 23 localhost

6. Allow SSH access (port 22):
   sudo ufw allow 22

7. Delete the test block rule (port 23):
   sudo ufw delete deny 23

8. Final status check to ensure rule is removed:
   sudo ufw status numbered

Summary:
UFW ek simple firewall management tool hai jo Linux me use hota hai. Isme hum port-based traffic ko allow ya block kar sakte hain.
Is task me port 23 (Telnet) ko block kiya gaya, fir SSH (port 22) allow kiya gaya aur finally test rule delete karke firewall ko original state me restore kiya gaya.

Required Screenshots:
1. Initial firewall status
2. Rule added (deny 23)
3. Status after adding rule
4. Telnet/Nmap test result
5. Rule deleted successfully
6. Final status (no port 23 rule)

Prepared by: Suraj Mishra
Date: 27 June 2025
