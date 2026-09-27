class AgentMemory:
    def __init__(self):
        self.memory = []
    def remember(self, fact: str):
        self.memory.append(fact)
        return f"Saved: {fact}"
    def recall(self, query: str):
        return [m for m in self.memory if query.lower() in m.lower()]

m = AgentMemory()
print(m.remember("Bhavagnitha loves Python"))
print(m.recall("Python"))
