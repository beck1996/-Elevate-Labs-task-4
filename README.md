# -Elevate-Labs-task-4
this Repo is related to internship task which explains how to block Ports in a firewall 
Step 1: Open Windows Firewall Configuration Tool
Press Windows Key

Search and open "Windows Defender Firewall with Advanced Security"

Step 2: List Current Firewall Rules
In the left pane, click on Inbound Rules

You'll see a list of all current rules (Name, Enabled/Disabled, Action)

Step 3: Add a Rule to Block Inbound Traffic on Port 23 (Telnet)
In the left pane, right-click Inbound Rules → click New Rule...

In the Rule Type window, select Port → click Next

Choose TCP, then select Specific local ports, type: 23 → click Next

Select Block the connection → click Next

Check all profiles (Domain, Private, Public) → click Next

Name the rule: Block Telnet Port 23 → click Finish

Step 4: Test the Rule
You can try connecting to port 23 using:

Telnet client (you might need to enable it via Windows Features)

Or use a port scanner like Nmap from another machine

If Telnet is blocked, connection will fail.

Step 5: (Skip – Linux only)
This step is for allowing SSH (port 22) on Linux.
Not applicable in Windows GUI.

Step 6: Remove the Block Rule to Restore Original State
Go back to Inbound Rules

Find the rule named "Block Telnet Port 23"

Right-click it → click Delete

Confirm deletion

Step 7: Document GUI Steps Used
Sample documentation:

Opened Windows Defender Firewall with Advanced Security

Navigated to Inbound Rules

Created a new rule to block TCP traffic on port 23

Applied the rule to all profiles

Deleted the rule after testing

Step 8: Summary – How Firewall Filters Traffic
The Windows Firewall GUI allows users to define rules for incoming and outgoing traffic based on ports, programs, or protocols. It evaluates network packets against these rules. If a packet matches a block rule, it is discarded. If it matches an allow rule, it's accepted. This helps prevent unauthorized access and protects the system from network threats.
