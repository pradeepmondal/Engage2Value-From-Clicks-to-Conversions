## Description
The goal of this competition is to predict a customer’s purchase value based on their multi-session behavior across digital touchpoints. The dataset captures anonymized user interactions such as browser types, traffic sources, device details, and geographical indicators. By modeling these patterns, participants will estimate the purchase potential of each user, helping optimize marketing and engagement strategies.

## Dataset Description
This dataset captures detailed session-level information from a large-scale digital commerce platform. Each row corresponds to a unique user session and includes data on user behavior, acquisition channels, device information, and geographical location.

Participants are expected to predict the purchaseValue, which represents the total amount spent during a given session.

### Key Feature Categories
#### User Behavior & Session Metrics

- totalHits, pageViews, totals.bounces, new_visits, totals.visits: Indicators of user engagement and session activity.
- sessionNumber, sessionStart: Information related to session sequence and timing.

#### Device & Technical Attributes

- deviceType, os, browser, screenSize, device.browserSize, device.language: Details about the user's device and browsing environment.
- browserMajor, device.*: Encompasses a variety of device-level descriptors such as model, version, and screen specifications.
- gclIdPresent: Signals the presence of a Google Click ID used in ad tracking.

#### Traffic & Marketing Source

- userChannel, trafficSource, trafficSource.medium, trafficSource.keyword, trafficSource.campaign: Insights into how users arrived at the platform.
- trafficSource.adwordsClickInfo.*: Contains attributes from advertising sources, including ad network type and slot.
- trafficSource.adContent, trafficSource.referralPath, trafficSource.isTrueDirect: Provide further attribution details.

#### Geographical Context

- geoNetwork.city, locationCountry, geoNetwork.continent, geoNetwork.subContinent, geoNetwork.metro, geoNetwork.region: Geographic identifiers to help understand regional behavior trends.
- geoCluster, locationZone: Groupings based on geographic or behavioral patterns.

#### Identifiers

- userId, sessionId: Unique identifiers for each user and session, allowing for multi-session analysis.

#### Target Variable

- purchaseValue: The amount (in currency units) spent by the customer during the session. This is the target variable to be predicted.

## Evaluation
Submissions are evaluated on r2_score() between the predicted values and the True target.

### Submission File
For each id in the test set, you must predict the target variable purchaseValue. The file should contain a header and have the following format:

id	purchaseValue
0	0
1	0
2	10990000
4	36500
5	0
etc.
