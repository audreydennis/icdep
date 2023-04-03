# How can we add additional features without breaking previous functionality?

Consider: 
- Send to any individual on the whole UW campus
- Specify whether contents are ASCII text, Unicode text, or binary values
- Keep a record of what nodes the card has passed through 
- Your extension mechanism should allow for any kind of extension we can imagine

**Content Type:**

To specify whether contents of the message are ASCII text, Unicode text, or binary values. Each card will have 3 letters in the upper left corner, with the number of the card written as fraction in the upper right corner, to dictate if the card is written in ASCII text, univode or binary. ASC for ASCII text, UNI for Unicode, and BIN for binary. The text content should be translated/interpreted based on this value. Originally I thought only the first card should state what type of content the text is, but then I realized each card needs to have the type specified in case the first card is lost or any card is lost and the reciever still needs to understand the message.

**Addresses:**

In order to send to any individual on the whole UW campus, each individual on the whole UW campus will have a specific assigned number or address associate with them depending on their location. The address will consist of three 4 digit numbers separated by a period and will be created as follows. The first number will be the building number, the second will be the room number and the third is the person number. Each building at UW has a specific 4-digit facility number as found on https://facilities.uw.edu/bldg. The second number is the room number within the building, and the third number is the number associated with the person. Each person will be assigned a number baised on how they entered the room. The first person in the room will be number 0001, whereas the hundreth person would be 0100. No room at UW to my knowledge has a capacity of over 1000, with the max capacity being Kane hall with 720 max. This address protocol will allow Alice to address a message to any individual on the whole UW Campus.

**Envelopes:**

Alice will place index cards in individual envelopes. On the envelope Alice writes both the individual address (as defined bellow) of the individual she is attempting to contact and her own address in case any envelope or card is missing and any node needs to contact her to request a replacement. The receiving address is written on the upper left corner and the sending address is written on the bottom left. The envelope also has the corresponding index card number, the fraction with number and message length, written on the upper right corner. This ensures if any envelope goes missing any node or the receiver will be able to request an exact replacement.

The envelopes also add additional privacy. Each node can't see whats written on the index card, therefore the message remains private between Alice and whoever she is contacting.

In this system someone will have to physically walk the envelope or envelopes, from the room Alice is in to the building that her recipient is in as dictated by the address.

**Record:**

In order to keep track of what nodes the card has passed through. Each node will write their specific address on the envelope in the bottom right corner. By the time the envelope reaches its destination it will have, the receving and sending address, the correspong card number, and the address of each node it passed through. This provides thorough information to the receiver and if anything is wrong with the envelope or it has been tampered with there is a full record of who all has interacted with it.



