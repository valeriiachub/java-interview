## Explain Session#evict() method
To detach the object from session cache, hibernate provides evict() method. After detaching the object from the session, any change to object won't be persisted. The associated objects will also be detached if the association is mapped with cascade="evict".
