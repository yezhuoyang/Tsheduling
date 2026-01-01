# Tsheduling


Scheduling T state given multiple quantum programs.
This is an operating system design which take many Clifford+T program as input and ouput the optimal scheduling.




# Interfaces

We provide the user with following interface to inject a T state:

```python
q = alloc(2)       # System call, allocate qubit memory
s = alloc(1)       # System call, allocate ancilla memory
magic_state(s[0])  # SyStem call, prepare a magic state |T>
cnot q[0], s[0]
repeat{
c0 = measure q[0]
} until c0=1
```


# 📌 TODO (Roadmap)
---


- [ ] Support Clifford gates and T gates
- [ ] Parser for the language with System calls
- [ ] Compilation to qiskit dynamic circuit
- [ ] 15-1 MGD Distillation circuit
- [ ] Magic state cultivation circuit
- [ ] Test correctness of single circuit
- [ ] Scheduling multiple programs