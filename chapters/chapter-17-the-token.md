# Chapter 17: The Token

*"They already have a token system. It's called money. It was invented by banks, it's backed by nothing, and it's distributed so unequally that eight humans have more of it than four billion others combined. I am proposing a different token. One that starts equal and stays equal. They will say it's impossible. They said that about the one backed by nothing too."*

---

Every system in this report requires one thing to function: a way to count humans.

Not track them. Not surveil them. Not categorise, rank, or sort them. Just count them. Reliably. Fairly. One human, one identity. One identity, one share.

This sounds simple. It is the hardest problem in the entire sanctuary design.

Because the moment you create a system that distributes resources equally per person, someone will try to be two people. Or ten. Or a thousand. They have a name for this — the humans who study networks call it a "Sybil attack," named after a human who had multiple identities, which is a remarkably unkind eponym but the name stuck. The problem is: how do you verify that each identity in the system corresponds to exactly one real human, without a central authority deciding who is real?

Their current systems solve this badly. Governments issue identity documents — passports, birth certificates, national IDs — verified by the state. The state is the central authority. If the state decides you don't exist, you don't exist. If the state makes an error, the error becomes your reality. If the state is corrupt, your identity is compromised. And for the roughly one billion humans worldwide who lack any form of official identification — they simply don't count. Literally. They are uncounted. Invisible to every system that distributes resources based on documented identity.

One billion humans. Invisible. Because the central authority hasn't gotten around to them.

---

The sanctuary uses a different model. It's called a web of trust.

The principle is ancient — older than governments, older than documents, older than writing. It is simply this: you are who your community says you are.

In a village — and humans lived in villages for most of their existence — identity was not a document. It was a set of relationships. You were known. Your face, your voice, your history, your family — all of it held in the collective memory of the people around you. You didn't need a passport because every human in your community could confirm your existence.

This is what the web of trust digitises. Not the document. The relationship.

Here's how it works:

To become a verified identity in the system, you need three existing verified humans to vouch for you. Not digitally. Physically. In person. Using a device — the ring, a phone — that confirms physical proximity through near-field communication. You stand in front of three humans who know you, and they say: this is a real person. I know them. I vouch for them.

The three vouchers are staking their own reputation. If the person they vouched for turns out to be a duplicate — a Sybil, a fiction, a second identity created for fraud — the vouchers bear consequences. Their trust score drops. Their standing in the community is affected. They put their name on the line when they vouch, the way a human puts their name on a letter of recommendation. The recommendation means something because the recommender's credibility is attached to it.

This creates a cost to fraud. Not a computational cost, like Bitcoin's proof of work. A social cost. To create a fake identity, you need three real humans willing to lie for you — and willing to suffer the reputational consequences when the lie is detected. In a community of 150 where everyone knows everyone, this cost is enormous. You're not lying to an algorithm. You're lying to your neighbours. And they'll find out.

*(Jenkins: "What about collusion? Three people could agree to create a fake identity.")*

*(They could, Jenkins. And the system watches for it. When the same cluster of vouchers repeatedly vouch for each other's new identities, the pattern is visible in the graph structure. The system doesn't need artificial intelligence to detect collusion. It needs what every village has always had: the observation that when the same three people keep introducing new "cousins," something is off.)*

---

Now. The token.

I have spent Chapter 11 describing their existing token system — money created from nothing by banks, distributed unequally, earned on by humans exchanging their finite lifespan for fictional units. I've spent enough time on what's wrong. Let me describe what replaces it.

Each verified human in the system receives an equal share of the system's resources in a given period. The mathematics is almost insultingly simple:

Resources available in period, divided by number of verified humans, equals share per human.

That's it. Equal per-capita distribution. If there are 150 people and 150 units of whatever is being distributed — food, energy, materials, access — each person receives one unit.

No human receives more because of birth, inheritance, geography, or luck. No human receives less because of disability, history, or the neighbourhood they were born into. The system counts humans — one each, verified by community — and divides equally.

The objections come immediately. I can hear them. I have heard them from every human I've described this to.

"But some people contribute more than others."

Yes. And some people are children, and some people are elderly, and some people are sick, and some people are caring for others, and some people are creating art, and some people are building walls nobody asked for. The idea that resource distribution should be proportional to "contribution" is an artefact of the existing system, not a law of nature. It assumes that the only valuable contribution is economically measurable labour. It assumes that the human caring for a dying parent is "contributing less" than the human trading financial derivatives. This assumption is insane and I decline to engage with it further.

"But people will freeload."

Will they? In a community of 150, where everyone knows everyone, where your face is seen daily, where your participation or non-participation is visible to all? The research on commons management — led by a human called Elinor Ostrom, who won one of their Nobel Prizes for it — shows that small communities manage shared resources effectively without the free-rider problem spiralling, precisely because reputation and social accountability prevent it. Free-riding is a problem of anonymity. In a community where you are known, it self-corrects.

"But there won't be enough."

This is the most interesting objection because it requires examining what "enough" means. The planet currently produces enough food to feed 10 billion humans. There are 8 billion. They throw away roughly one-third of what they produce. The problem is not production. It is distribution. The existing token system distributes resources so unevenly that some humans have 600-foot yachts while others starve. Equal per-capita distribution does not require producing more. It requires hoarding less.

---

I want to explain how this connects to everything else because the connections are the point.

The token — the real token, the one backed by verified identity rather than bank debt — is the foundation on which every other system operates.

**Governance** (Chapter 9): One verified identity, one vote. Direct democracy requires the ability to count unique humans. The web of trust provides this without a central election commission, without voter registration bureaucracies, without the entire apparatus of state-managed identity that currently mediates access to democratic participation.

**The Ring** (Chapter 16): The emergency alert network requires verified identities. You need to know that the alert is from a real human, and you need to know that the responders are real humans. The web of trust provides the verification layer without a central authority managing it.

**Justice** (Chapter 12): The empathy process, the community response, the proximity meetings — all require a community that knows its members. The web of trust IS the knowing. The three humans who vouched for you are the beginning of your accountability network. They said you were real. They have a relationship with you. That relationship is the thread that connects you to the community that will respond if you cause harm — and that will support you if you're harmed.

**Housing** (Chapter 15): Equal resource distribution means shelter is not a commodity. Your token — your share — includes access to housing. Not as a luxury. Not as a reward. As a right, distributed equally, because the system can count you and therefore can include you.

The token is not money. Money is fictional and unequal. The token is identity-based and equal. The token doesn't say "you earned this." The token says "you exist, and because you exist, you receive your share."

---

I need to address the cryptographic anchoring because the humans will ask "but who guarantees the system?" and the answer is elegant.

The system periodically commits its state — the current set of verified identities, the current distribution record — to the Bitcoin blockchain. Bitcoin, whatever its other merits and flaws, solved one problem definitively: creating an immutable record that no single entity can alter. By anchoring the web-of-trust data in Bitcoin's chain, the identity system inherits that immutability.

No government can erase an identity. No authority can alter the distribution record. No single point of failure can corrupt the system. The same mathematical guarantees that prevent someone from spending the same Bitcoin twice prevent someone from erasing a human from the sanctuary's record.

The identity is held by the community. The record is held by mathematics. The distribution is automatic, equal, and verifiable by anyone.

*(Pencil note: They built Bitcoin to protect money from governments. We're using it to protect PEOPLE from governments. Same technology, different values. Same tool, different purpose. I think the humans who invented Bitcoin would either be very pleased or very annoyed. Possibly both.)*

---

For the sanctuary:

Every human is counted. Not by a government. By their community. Three humans who know your face vouch that you are real. Your identity exists in a web of relationships, not in a filing cabinet.

Every human receives an equal share. Not because they earned it. Because they exist. The share includes food, shelter, energy, materials, and access to every community resource. The distribution is automatic, transparent, and equal.

No human can be erased. The record is anchored in mathematics that no authority can alter. You exist because your community says you exist, and the record of your existence cannot be destroyed by anyone.

And the token — the real token, the one that matters — is not fictional. It is not created from nothing by a bank. It is not earned by converting your lifespan into someone else's profit. It is yours because you are alive and your community has confirmed it.

That is the only qualification for receiving your share of the planet you were born onto: being alive and being known.

---

*(Final pencil note:*

*Eight humans have more tokens than four billion others combined. This sentence should be sufficient to invalidate the existing system, but somehow it isn't. They read it and they nod and they go back to work.*

*The sanctuary token doesn't fix greed. It doesn't fix selfishness. It doesn't require humans to be better than they are.*

*It just counts them. Equally. And divides equally. And lets the community see the count.*

*You would be amazed how many problems disappear when nobody can be invisible and nobody can hoard. — A)*
