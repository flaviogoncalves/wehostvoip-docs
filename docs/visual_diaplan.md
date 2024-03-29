# Visual Dialplan

The Visual Diaplan is one of the greatest differentiators of the system. It is simple to use and vizualize. The call will go thru node by node doing all the telephony functions such as playback, ivr and others.  

The first screen of the dialplan is to create or open it and to define timezone and timeperiod. 

<img src="https://user-images.githubusercontent.com/4958202/148941326-41d8f50b-f1e7-428f-9f87-ff133658c24c.png" width="480">

If you decide to create a new Visual Dialplan, fill the name, the timezone and the time period. This is very important.  Once you have selected this parameters you can start creating your Visual Dial Plan

![image](https://user-images.githubusercontent.com/4958202/148945818-aa6fe3a2-345d-4503-82a0-24dfcde0bbb2.png)

In the figure above you can see the main commands of the Visual Dial Plan Editor

The first buttons are the simplest

* New
* Open
* Edit Info (Timezone, Time Period,  Name)
* Save
* Undo
* Redo
* Arrange
* Upload JSON (Pro Edition)
* Download JSON (Pro Edition)

In the system you can organize the boxes in a logical way to process your incoming calls. Let's see an example below.

![image](https://user-images.githubusercontent.com/4958202/148946911-c2860fb9-2f20-4209-8d12-498ae46f7858.png)

There are different types of block to build your visual dialplan. I'm going to list them below, by clincking in the link you will have a more detailed view of each block

* [Start](#start)
* Group
* Hangup
* Ivr
* Playback
* Say
* Subscriber
* Timerouting
* Voicemail
* Visual Plan

# Start
The block start is just the starting point of the Visual Dial Plan (VDP). It is automatically positioned in the VDP.

![image](https://user-images.githubusercontent.com/4958202/148984484-dcefe8ed-b0b4-42d0-ba6b-64d6507121af.png)

# Group
Group is similar to a queue. It will ring on all phones at the same time. For serial hunt groups you may use the subscriber block. 

![image](https://user-images.githubusercontent.com/4958202/148984695-ead6e82d-5c46-4362-b197-c6a0fef99939.png)

# Hangup
Disconnect the call.

![image](https://user-images.githubusercontent.com/4958202/148984900-03704c89-71df-4d46-8a95-ac95251bd0e5.png)

# IVR
Interactive Voice Response or IVR is one of the most sophisticated blocks of the VDP.

![image](https://user-images.githubusercontent.com/4958202/148985005-bc03f981-eaf1-45ec-b8fd-bdfa9fcd1382.png)

The main options of this block:

* Auto-Attendant - If you select auto-attendant, the system will allow you to dial the extension to go directly to the subscriber
* Timeout - Time to wait for a dtmf input
* Type - If _Audio Library_ where you can select a pre-recorded audio or text-to-speech if you prefer to generate the text on the fly.
* Insert Audio - Only if audio library. Select a pre-recorded audio (Formats wav and mp3)
* Text - Text to be played. Once played, the audio will be cached to avoid regeneration. 
* Language - Select the languages supported
* Text-Type - [SSML](https://en.wikipedia.org/wiki/Speech_Synthesis_Markup_Language) Speech Synthesis Markup Language or Text
* Sentence-Type - Sentence, SSML and Word
  * word – Indicates a word element in the text.
  * ssml – Describes a <mark> element from the SSML input text. For more information, see Generating Speech from SSML Documents. 

# Playback

Playback is a block to play a messages or generate a message based on text to speech. 

![image](https://user-images.githubusercontent.com/4958202/154244210-75716333-a5d6-41da-8fe3-1ba8b0461a97.png)
 
The main options of this block are:

* Type - If _Audio Library_ where you can select a pre-recorded audio or text-to-speech if you prefer to generate the text on the fly.
* Insert Audio - Only if audio library. Select a pre-recorded audio (Formats wav and mp3)
* Text - Text to be played. Once played, the audio will be cached to avoid regeneration. 
* Language - Select the languages supported
* Text-Type - [SSML](https://en.wikipedia.org/wiki/Speech_Synthesis_Markup_Language) Speech Synthesis Markup Language or Text
* Sentence-Type - Sentence, SSML and Word
  * word – Indicates a word element in the text.
  * ssml – Describes a <mark> element from the SSML input text. For more information, see Generating Speech from SSML Documents. 

# Say
The say application will use the pre-recorded sound files to read or say various things like dates, times, digits, etc.

 ![image](https://user-images.githubusercontent.com/4958202/154244296-89646e52-62fd-4923-9ef6-cd8bf05c4bd4.png)
 
It can read digits, numbers, dollar amounts, date/time values, IP addresses, spell out alpha-numeric text, including punctuation marks, and so on.

## type 	

* NUMBER    |
* ITEMS     | general counts
* PERSONS   |
* MESSAGES  |
* CURRENCY    | money-related
* TIME_MEASUREMENT    |
* CURRENT_DATE        |
* CURRENT_TIME        | dates and times
* CURRENT_DATE_TIME   |
* SHORT_DATE_TIME     |
* NAME_SPELLED    | spelling
* NAME_PHONETIC   |
* TELEPHONE_NUMBER
* TELEPHONE_EXTENSION
* URL
* IP_ADDRESS
* EMAIL_ADDRESS
* POSTAL_ADDRESS
* ACCOUNT_NUMBER

## method 	

* pronounced - cardinal number, e.g. "forty two"
* iterated - nominal number, e.g. "four two"
* counted - ordinal number, e.g. "forty second"

# Subscriber

The subscriber box, delivers the message to a subscriber or subscribers. If you define more than one subscriber, the application will ring both subscribers simultaneously like a ring-group. If you prefer you can chack the box serialize and the system will ring the subscribers in sequence sych as a hunt-group. 

![image](https://user-images.githubusercontent.com/4958202/154244438-d2d0ecbf-b8b3-4ace-8369-c18c0ed950e2.png) 
 
# Timerouting

Timerouting is a simple box it has only two exits. It uses the business hours defined previously to determine if it is on busines hours or not. When you create the visual dialplan you have to specify the business hours.

![image](https://user-images.githubusercontent.com/4958202/154244562-779c1693-80f2-4a39-9f23-7d361c2e786f.png)
 
# Voicemail 

We have made our voicemail as simple as possible. The voicemail box simply recirds a message and send it attached to the email of the user. There are no extensions to dial or password to recover, no maintenance of the mailbox. This system was designed to be simple and we have simplified the voicemail. 

![image](https://user-images.githubusercontent.com/4958202/154244925-68531c53-3af1-46b7-9e8f-413ee5c41dc3.png)
 
# Visual Plan

The visual plan box allows you to call other visual plan  from the same interface. 
 
![image](https://user-images.githubusercontent.com/4958202/154244993-3ec1aec1-7cb9-4a81-be66-73e0557facda.png)
