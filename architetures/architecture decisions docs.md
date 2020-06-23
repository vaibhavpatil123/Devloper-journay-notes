“We will keep a collection of records for architecturally
significant decisions: those that affect the structure, non
functional characteristics, dependencies, interfaces, or
construction techniques.”
- Michael Nygard

http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions

Example 
1. Asynchronous messaging between bidding services
 
## Status
Proposed

## Context

The Bid Capture Service, upon receiving a bid from an online bidder or from a live bidder via the auctioneer,
must forward that bid onto the Bid Streamer Service and the Bidder Tracker Service. This could be done
using async p2p or pub/sub

## Decision

We will use asynchronous messaging between the Bid Capture Service, Bid Streamer Service, and the
Bidder Tracker Service.
The Bid Capture Service does not need any information back from the Bid Streamer Service or Bidder
Tracker Service.
The Bid Streamer Service must receive bids in the exact order they were accepted by the Bid Capture
Service. Using messaging and queues automatically guarantees the bid order for the stream.

## Consequences

We will require clustering and high availability of the message queues
Internal bid events will be bypassing security checks done in the API layer.
