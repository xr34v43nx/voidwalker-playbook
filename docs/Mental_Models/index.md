## Mental Models of Protocols

These are human analogies I use to internals how protocols behave.
They are not replacements for technical definitions, but intuition-building tools that help me reason about behavior during enumeration, exploitation, and debugging.

### TCP — Top Chap Percival

TCP feels like Top Chap Percival.

Percival is a proper top chap. He sends letters to request a meetup time and waits patiently for a reply before proceeding. Every exchange is acknowledged. If something goes missing, Percival notices and asks for it again.

He is punctual, methodical, and polite.

We arrange our business carefully, and as parcels and letters pass between our estates, Percival keeps itemized dossiers of everything that was sent and received. He ensures both parties agree on what was exchanged and in what order, and nothing moves forward until both sides confirm understanding.

This maps well to TCP’s behavior:

- Connection-oriented communication
- Acknowledgements for received data
- Re-transmission when something is lost
- Ordered delivery
- Reliability over speed

TCP prioritizes correctness and completeness, even if that means things take longer.

### UDP — Unsupervised Drunk Person

UDP feels like an Unsupervised Drunk Person.

Messages are sent rapidly and enthusiastically, but with no confirmation that they were received. There is no waiting for replies, no checking if something was missed, and no concern for order.

Sometimes the message arrives.
Sometimes it doesn’t.
Sometimes it arrives twice.
Sometimes it arrives out of order.

And UDP simply keeps going.

This reflects UDP’s nature:

- Connectionless communication
- No acknowledgements
- No retransmissions
- No guarantees of order or delivery
- Speed over reliability

UDP doesn’t care if you heard it — only that it shouted.

### TLS — Timid Little Shadow (The Leet Spy)

TLS feels like a Timid Little Shadow — or perhaps The Leet Spy.

It operates quietly in the background, ensuring that whatever is being said cannot be understood by anyone else listening. You don’t always notice it, but it is constantly present, wrapping communication in secrecy and trust.

Before anything meaningful happens, TLS insists on introductions:

- Who are you?
- Can I trust you?
- Can we agree on how we’ll speak securely?
- Only once this handshake is complete does real communication begin.

TLS isn’t about moving data faster or more efficiently — it’s about ensuring:

- Confidentiality (no eavesdropping)
- Integrity (no tampering)
- Authenticity (you are who you say you are)

TLS doesn’t change what is said — it changes who is allowed to understand it.

## SSL — Sentry Stationed Lair

A guarded location where communication is only allowed after identity is verified and rules of engagement are established.

Mental Model

SSL behaves like a fortified meeting chamber:

- A sentry challenges anyone attempting entry
- Credentials and capabilities are checked before entry is granted
- Once inside, communication is private and protected from eavesdroppers

Outsiders can see that something is happening, but not what

The key idea is not encryption itself, but controlled access to a trusted channel.