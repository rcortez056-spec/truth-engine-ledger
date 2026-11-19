# Truth Engine: Append-Only Ledger (Demo)

A browser demo of an append-only event ledger. Entries are added in order and are not edited or deleted through the interface.

**Live demo:** https://immutable-3-ramon.netlify.app

## What the demo does

- **New Transaction:** adds four entries for one transaction: RECEIVED, LOCKED, EXECUTING, SUCCESS.
- **Query Full History:** shows every entry for a transaction ID.
- **Verify Chain Integrity:** checks the links between entries.
- **Reset Demo:** clears the demo ledger. This control exists only for the demo.

## Rules the demo follows

- Entries are added with INSERT only.
- UPDATE, DELETE, and overwrite are not available in the interface.
- Each entry stores a hash of its contents and the hash of the entry before it.

## Status

Prototype. Single HTML file that runs in the browser. The hash is a simple demo function, not a cryptographic one, so it does not prove tampering. Data is held in memory and resets on reload. Not a production audit system. Not connected to Sentinel Guard Engine.

## Not built yet

- Persistent storage
- Cryptographic hashing (SHA-256)
- Server-side enforcement of append-only writes

## Stack

HTML, CSS, JavaScript. Hosting: Netlify.
