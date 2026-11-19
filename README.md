AI Usage:

Lab 4:
1. The drop rule was added without priority, so it is the same priority as the forwarding rule. An ICMP packet matches the forwarding rule first, so it is sent out. Blocking h1 → h3 also breaks h3 → h1 because a ping needs a reply.
2. h1 → h2 had already been seen in Step 4, so the controller had installed specific flows for it, with idle_timeout=60. Those flows stay in the switch’s table after the controller dies. h1 → h3 was a new conversation with no matching flow.
3. Secure, especially on switches that enforce security policy. In secure mode, the controller’s rules stay in force when the controller is unreachable. Standalone mode risks the controller’s policy disappears if an outage happens.