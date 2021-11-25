


![ATty](https://user-images.githubusercontent.com/83019866/143379831-fdeb0cf7-4721-4253-8452-27f40aaea328.png)



   
   / \|_   _| |_ _   _
  / _ \ | | | __| | | |
 / ___ \| | | |_| |_| |
/_/   \_\_|  \__|\__, |
                 |___/						

ATty is an tool that can used with any 2G/3G/4G USB dongles. This tool can test basis device features such as network connection, make/receive voice calls, send/receive SMS, network selection etc. In addition the tool has enhanced diagnostics features that can be used to troubleshoot network or device issues.
-
ATty is a JavaFX based Open-Source tool that works fine with JavaSE 8. The tool can automatically detect and connect to the modem device connected to the computer. This tutorial will explain how to use ATty to test device features and troubleshoot issues.
-
Connect the Device

Install the drivers for the device that is provided by the manufacturer. In most cases, the drivers packaged as part of the device connection manager application (ex ‘Mobile Partner’ for Huawei USB modems).Now connect the device to your computer. When you press ‘AutoConnect’, ATty will check the all the available ports on the computer and try to connect to thde modem device. You can also press ‘Find Ports’ and connect the device’s AT Command Port if you have that information avaialble.
-
Diagnostics

In the ‘Diagnostics’ tab, you can get useful diagnostics information about the device and the network. This can help troubleshoot many of the common issues seen by users.Steps to get more additional diagnostics data will be explained later.
-
Network Connection

Network connection can be tested under the ‘Data Call’ tab. In order to connect to the network, a connection profile (PDP Context) should created. Create a connetion profile as shown below. APN information is network specific, usually you can search the google (ex. “AT&T APN”) to get that information. Once the connection profile is created, just press the ‘Connect’ button. To test whether is connection is sucessful, press ‘Show IP Address’ button.
-
Voice Call

With ATty you can make/receive voice calls on modems that support this feature. For outgoing call, enter the number and press the ‘Dial’ button in the ‘Voice Call’ tab. For incoming calls, ATty will automatically detect the incoming call and alert the user.
-
SMS

SMS messages can be sent through ATty. In the ‘SMS’ tab, enter the phone number and the message and just send. You can also read the stored SMS messages from teh device. Currently only ‘Text Mode’ messages are supportes, ‘PDU Mode’ message is not supported. You can check the SMS Message setting in the ‘Diagnostics’ tab.
-
Common Troubleshooting Steps

In the ‘Diagnostics’ tab, you can perform the following diagnosis:

-Is the SIM properly inserted?
-Check the ‘SIM Status’. If you get the ‘SIM is ready’ message, the SIM card is properly inserted and          ready.
-  
What is the signal condition of the device?
Check the ‘Signal Strength’. You’ll get a qualitative response about your signal condition. You can can adjust your position of the device to get a better signal coverage.
-
Is the device Roaming?
Check the ‘Registration’ status. It will check whether the device is registered with the network and whether it is roaming or in the home network.
-
Is the device connected to the network?
Check the ‘Conn. Status’. It will check if the device is connected to the network.
-
What is the current operator?
Check the ‘Operator’ info.
-
What is the current IP address?
Check the ‘IP Address’. Only if teh device is sucessfully connected to the network, a valid IP address will be available.
-
Does the device support SMS?
Check the ‘SMS Support’. Also confirm the ‘SMS format’ setting on teh device. Eventhough the device is capable of SMS, the SIM account should have SMS feature enabled for that feature to work.
-
Does the device have the right connection profile for the network?
Check the ‘Conn. Profiles’. The correct APN information is needed to connect to the operator. Each operator has a unique APN. Usually that information can be found through Google search. Use the ‘Data Call’ tab to add/edit connection profiles.
-
I’m unable to connect to the internet. What should I do?
#1 Check the ‘Signal Strength’. If you have no coverage, you cannot connect to the internet.
#2 Check the ‘Operator Info’. The device should be sucessfuly registered with a operator.
#3 Check the ‘Registration’. The device should be sucessfully registered with the home or roaming network.
#4 Check the ‘Conn. Profiles’. A proper conenction profile should be setup for the operator. The correct APN information for the operator should be used in the ‘PDP Profile’ that is used for the connection.
#5 Check the ‘Attach Status’. The device should sucessfully attach to teh network before it can connect to the internet. If the Attach is unsucessful, please check the SIM account with the operator.
-
Advanced diagnostics for Huawei Modems
To get advanced diagnostics info. for Huawei modems, please send the following commands in the ‘Script Mode’ tab of the ATty.
-
//Get the System info
AT^SYSINFO
-
//Cardlock status
AT^CARDLOCK?
-
//Frequency Preference
AT^FREQPREF?
-
//Frequency Lock
AT^FREQLOCK?
-
//Card mode
AT^U2DIAG?
-
//Read SPN file
AT^SPN?
