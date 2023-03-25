24-03-2023  21:03

*Status* : #incomplete 

*Tags* : 

# Theorem Forms are not enough

---

## My vision

 The formalisation of mathematics could lead to a future where we might be able to do semantic search of "theorem forms" that we as human prover would be guessing.

> [!note]
> What I meant to say is we can automate aspects of our job as a researcher where we might be able to fetch theorems already proven that look similar. I thought this could be done.


----
## Abhisekh's Rebuttal

 ```mermaid
 graph TD
 
 id1(Proof)
 id2.1(computable)
 id2.2(non computable)
 id3.1(exponential sized)
 id3.2(polynomial sized)
id1 --> id2.1
id1 --> id2.2
id2.1 --> id3.1
id2.1 --> id3.2
```

The above idea at least as stated does not help because, `same theorem forms` may have computable and non computable `proofs` at the same time! Thus `context` or `domains` where the theorem form is interpreted matters a lot.

>[!Example]
> $\exists$ - Theory of $(\mathbb{N},+,\times)$ is undecidable - Matijasevich's theorem
> $\exists$ - Theory of $(\mathbb{R},+,\times)$ is decidable - Tarski's Theorem


---
## Bottomline

This idea needs further refinement.

---
### References
1.  Discussion with Abhisekh 24-03-23, on discussion the motivation poetry for my TIFR application.
2. [My math stackexchange query](https://math.stackexchange.com/questions/4663259/software-recommendation-for-theorem-suggestions?noredirect=1#comment9852236_4663259)