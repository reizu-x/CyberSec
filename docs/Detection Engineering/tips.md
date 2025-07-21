# Detection Tips

## Questions

: Questions to ask when setting up a detection.

- What are we trying to protect?
- What are the threat against that?
    - What are our exposure?
    - What are our risks?
- What are our mitigation options?
    - Isolation Area?
    - Contact the Owner?
    - etc etc

---

## Tips

- Detections on the entire chain over Detections that covers MITRE
    - Start from the last part of the Kill Chain is more logical, from actions on objectives to Initial Access.
        - Start on the things you don't want to happen, then continue upwards.

- Automate, Every possible thing.
- Threat Intelligence is simply a ton of data.
    - Automate it to enrich and tell them that it is in the list.
    - CTI is only for context.
    - Tactics and Techniques
        - Are we targeted?
        - Invest in area that are targeting you, based on the industry.

- Threat Research is a big part of the job.

---

## Security Detection Lifecycle

1. Determine what you ahve to work with
2. What threat do you want to detect? Reference MITRE ATT&CK
3. Research the threat in your environment and externally
4. Build the logic & test your hypothesis
5. Evaluate next steps (documentation, peer review, etc.)
    - What spurs detection writing?
        - Threat Hunting
        - Security Incident
        - New Asset or Regulation
6. Testing your detection
    - Run your newly written detection in a testing environment
    - Does it detect the behavior you wanted it to?
    - Are there any false positives?
    - What can be improved?
7. Evaluate the Detection
    - If you believe the detection should be in production, document all your reaserch and testing!
8. Then...
    1. Pass it on for peer feedback from your teammates.
    2. Write a playbook with the threat scenario and specific actions that can be taken to investigate this alert.
    3. Evaluate if response can be automated.
