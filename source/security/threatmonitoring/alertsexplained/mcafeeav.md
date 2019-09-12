```eval_rst
.. meta::
     :title: McAfee Anti Virus Rules Explained | UKFast Documentation
     :description: Our Threat Monitoring ruleset explained
     :keywords: threat monitoring, alerts, security, compliance, rules, rulesets, ukfast, hosting, file integrity monitoring, rootkit, detection, vulnerability scan, scans, hids, intrustion detection, set up
```

# McAfee Anti Virus

##  McAfee Windows AV - Virus detected and not removed.

###  What does this rule mean?


Triggered when McAfee Windows AV was unable to remove a virus, this rule should be acted upon quickly. This indicated that a virus was detected, but for some reason was not successfully removed. This could be due to the virus preventing the anti-virus application from removing it. Alternatively, and more commonly, the anti-malware program may not have the right permissions to remove the malware.

As a side note, we regularly see McAfee Windows Anti-Virus trigger this rule when it did actually remove the malware successfully. We recommend always double checking manually and taking any action as needed.

Many attackers follow an attack with malware. Installing a trojan, backdoor or, rootkit or RAT on your server is high on an attackers priority list. Should they be discovered, and the exploits patched, this malware could allow the attacker to regain access to your server, potentially bypassing authentication and auditing techniques.

### What triggers this rule?


One of the most common triggers for this rule is unwanted software that is installed along with third-party applications, ranging from Tool Bars to viruses like the infamous PCOptimiserPro Trojan. This rule can also be triggered by legitimate software. This can happen when Windows doesnt recognise an application or the software acts in a similar way to a virus (such as installing updates by connecting to an external IP in an obscure way.

Additionally, malware may have infected the system from other sources, like succeeding an attack, through a malicious email or suspicious file. After the initial malware event has been dealt with, the Threat Monitoring team is on hand to provide support when investigating further into the origins of malware.

### What action do I need to take?


As a first responder, you should log into the server in question to determine whether the file in question was deleted by the anti-virus software. If it was successfully removed, we recommend manually running a system scan to check for any remnants of the malware. Should the malware be present on the system still, it should be removed, either through the anti-virus programs quarantine features or manually? Once this has been done another system scan should be run. 




