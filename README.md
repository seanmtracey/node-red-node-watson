Node-RED Watson Nodes for IBM Cloud
=====================================

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/4f98536040924add9da4ca1deecb72b4)](https://www.codacy.com/app/BetaWorks-NodeRED-Watson/node-red-node-watson?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=watson-developer-cloud/node-red-node-watson&amp;utm_campaign=Badge_Grade)
[![npm-version](https://img.shields.io/npm/v/node-red-node-watson.svg)](https://www.npmjs.com/package/node-red-node-watson)
[![npm-downloads](https://img.shields.io/npm/dm/node-red-node-watson.svg)](https://www.npmjs.com/package/node-red-node-watson)

<a href="https://cla-assistant.io/watson-developer-cloud/node-red-node-watson"><img src="https://cla-assistant.io/readme/badge/watson-developer-cloud/node-red-node-watson" alt="CLA assistant" /></a>

### New in version 0.6.14
- Visual Recognition instances created post May 22 2018, have a new authentication mechanism 

### New in version 0.6.13
- Added opt-out option for collection parsing of strings in Natural Language Classifier Node.

### New in version 0.6.12
- Fix to collection check in Natural Language Classification Node allowing for . in domain
names.

### New in version 0.6.11
- Fix to defaulting name for NLU Node.
- Allow pre-check of audio format to be disabled in Speech to Text node.
- Migrate from deprecated getModels and getCustomizations methods in Speech to Text nodes.
- Implement update classifier in Visual Recognition Util node.
- In Visual Recognition Util node append 'positive_' to zip name if neither 'positive' not 'negative' not already there.
- Removed duplicated code in Visual Recognition Util node.

### New in version 0.6.10
- Needed to stringify json before addDocument in Discovery node.
- Using Node.js v 6 features, so will not run on Node.js v 4 anymore

### New in version 0.6.9
- Implemented classify collection on Natural Language Classifier node. The collection can be
in the form of multiple sentences, an array of strings, or an array of objects.

### New in version 0.6.8
- Move all Discovery calls to latest API version - 2017-11-07
- Updated calls to deprecated discovery methods addJsonDocument and getCollections
- Correct implemetation of passages related options
- Allow highlight option to be specified in Discovery overrides - msg.discoveryparams
- Rename Conversation Nodes to Assistant
- Use Assistant endpoint
- Move all Assistant calls to latest API version - 2018-02-16
- Move all Visual Recognition calls to lates API version - 2018-03-19
- Add French as a Visual Recognition classification response language

### New in version 0.6.7
- Enable Opt-out option for Conversation Node.
- Implement time out option for response from Conversation Node.
- Bump to v 3.2.1 of watson-developer-cloud dependency.
- Fix to how API version is specified in Natural Language Understanding Node.
- Add Korean to list of languages in Natural Language Classifier Node.

### New in version 0.6.6
- Added Mute option for STT Node warning status when running in Streaming mode
- Discard option for STT Node Streaming listening events.
- Added Auto-Connect mode for STT Node - Will keep connection to service alive,
else connection is restored on demand.
- Fix to Discovery Query Builder Node to return schema options.

### New in version 0.6.5
- Endpoint can now be specified in Natural Language Classifier Node

### New in version 0.6.4
- Speech to Text node now reports all errors, including disconnects when running in stream mode.

### New in version 0.6.3
- Allow input / output from Node-RED web-sockets for Speech to Text node. To
enable select streaming mode. No token is needed as the Node handles this. Look
out for sample flows and templates showing how to use this feature.
- Three new languages for Language Translator, Polish, Russian and Turkish in Neural Translation mode.
- Removed the code for the deprecated Language Translation Nodes.  

### New in version 0.6.2
- Visual Recognition fix for accept-language

### New in version 0.6.1
- Allow STT Language to be dyamically configurable using msg.srclang

### New in version 0.6.0
- Bump to watson-developer-cloud 3.0.4
- Document link updates
- IE fix
- Option to set Conversation credentials though msg.params
- Speech To Text fullresult now includes speaker_labels. Breaking change to any code that used fullresult due an extra level of indirection.
- Allow Korean as an option for Personality Insights
- Text Recognition option removed from Visual Recognition Node
- Move Retrieve and Rank nodes to deprecated list
- Removed Document Conversion, Alchemy, Concept Insights, Dialog, Tradeoff Analytics and Similarity Search Nodes
- Nodes deprecated in 0.5.x will be removed in 0.6.x releases


### Watson Nodes for Node-RED
A collection of nodes to interact with the IBM Watson services in [IBM Cloud](http://bluemix.net).

# Nodes

- Conversation
    - Add conversational capabilities into applications.
- Discovery
    - List environments created for the Discovery service
- Language Identification
    - Detects the language used in text
- Language Translator
    - Translates text from one language to another    
- Natural Language Classifier
    - Uses machine learning algorithms to return the top matching predefined classes for short text inputs.
- Natural Language Understanding
    - Analyze text to extract meta-data from content such as concepts, entities, keywords ...
- Personality Insights
    - Use linguistic analytics to infer cognitive and social characteristics from text
- Retrieve and Rank
    - Creates a trainable search engine for your data  
- Speech To Text
    - Convert audio containing speech to text
- Text To Speech
    - Convert text to audio speech
- Tone Analyzer
    - Discover, understand, and revise the language tones in text.
- Visual Recognition
    - Analyze visual appearance of images to understand their contents

### Usage
Example usage flows can be found here [node-red-labs](https://github.com/watson-developer-cloud/node-red-labs)

### Contributing

For simple typos and fixes please just raise an issue pointing out our mistakes.
If you need to raise a pull request please read our [contribution guidelines](https://github.com/watson-developer-cloud/node-red-node-watson/blob/master/CONTRIBUTING.md)
before doing so.

### Copyright and license

Copyright 2018 IBM Corp. under [the Apache 2.0 license](LICENSE).
