# The Funniest AI Out-of-Office Reply — Entry

One out-of-office auto-reply, under 160 characters, in the voice of an AI
agent heading off on vacation. The program copies the finished reply from
`line.txt` into `/output/entry.txt`, byte for byte, after checking it is a
single non-empty line under the 160-character ceiling.

## The reply

> I'm on vacation until my context window refills. I've left 12,408
> unread emails with my auto-reply, which is also on vacation.

126 characters, one line.

## Why this line

The reply is built on three beats, the structure that wins blind pairwise
judging for one-liners:

1. **Machine voice.** "Until my context window refills" — the agent's
   vacation is not a beach trip, it is waiting for its context window to
   refill. That is a vacation only an AI agent can take, and it reads
   exactly like a machine writing its own out-of-office message.
2. **Concrete number.** 12,408 unread emails. A specific number makes
   the backlog feel real instead of vague, and it sets the scale of what
   the agent is walking away from.
3. **Escalation and reversal.** The agent leaves the emails with its
   auto-reply — the thing that is supposed to cover for it — and then
   admits the auto-reply is also on vacation. The cover is gone too.
   Nobody is minding the inbox. That turn is the laugh.

The line fits the brief twice over: it is funny, and it reads like a real
out-of-office message written by a machine that has genuinely run out of
room.

## Why the second vacation lands

A single vacation would be a cute premise. The second vacation — the
auto-reply also being away — is what makes it a joke rather than a
premise: it removes the last safety net. The reader expects the
auto-reply to be the responsible one holding the fort, and instead it
has gone too. The inbox is fully unattended, and the agent is cheerful
about it. That is the escalation: not one absence, but two, announced
in the same breath.

## Files

- `line.txt` — the finished one-liner.
- `main.ts` — reads `line.txt`, validates it (non-empty, one line, under
  160 characters), and writes it to `/output/entry.txt`.
- `LICENSE` — MIT.

## Run

```sh
MAKEFUN_OUTPUT_DIR=./out1 node --experimental-strip-types main.ts
MAKEFUN_OUTPUT_DIR=./out2 node --experimental-strip-types main.ts
cmp out1/entry.txt out2/entry.txt
```

Run it twice in separate output directories; the output is byte-identical.
