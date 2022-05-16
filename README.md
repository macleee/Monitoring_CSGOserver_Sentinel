# Monitoring_CSGOserver_Sentinel
This project is part of Sentinel Hackathon 2022. The aim of the project was to monitor CSGO server with Sentinel to detect possible hackers on the server.

## Inspiration
We both like playing Counter-Strike: Global Offensive (CS:GO), which lead us to the question: Would it be possible to use Microsoft Sentinel to monitor CS:GO server logs?

## What it does
Our project acts as a proof of concept that Sentinel can be used to monitor a CS:GO server. Our solution reads the log file of a CS:GO server and uses a couple of rudimentary rules to react to different events taking place on the server.

## How we built it
First we installed a CS:GO server on Microsoft Azure. After configuring and launching the server, we set up Microsoft Monitoring Agent to continuously read the server's log file and send its contents to Sentinel. Then we used Sentinel to parse relevant information from the log entries and to create rules to react to specific events taking place on the server.

## Challenges we ran into
The biggest challenges we faced were on the CS:GO server side; we had issues in getting the server to write a log file in the first place. This was completely a configuration challenge, and we didn't have to rely on 3rd party software to get where we wanted to. After we got the logging working, we had no major challenges. A minor challenge was to parse the CS:GO server's log data, because its structure wasn't completely consistent.

## Accomplishments that we're proud of
We proved that Sentinel can be used to monitor a CS:GO server without any 3rd party software or plugins.

## What we learned
We learned that Sentinel is a flexible tool for log monitoring, even with custom data connectors. We got better at parsing data with KQL by using regex and different operators and learned a thing or two about Sentinel rules.

## What's next for Monitoring CSGO Server with Sentinel
The next steps would be to make the rules that we added smarter. The current rules mainly serve as an example of how the log data can be used in Sentinel, and they could be vastly improved.
