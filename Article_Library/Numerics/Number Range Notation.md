---
title: Number Range Notation
tags:
  - math
concepts: inclusive range, exclusive range
---
# Number Range Notation

WMB employs a compressed symbolic notation for expressing range relationships, logical connections, and modal constraints. This keeps all operations in a consistent visual and syntactic format. The sections below define these conventions in both rendered and plaintext forms (when needed).

## Range Connectives

**Interior (Conjunction)**:

* *Inclusive-Inclusive*
$$(a \leq x;\;x  \leq b)$$
- Value must lie **inside** the range between *a* and *b*, **including both** *a* and *b*.

* *Exclusive-Inclusive*
$$(a < x;\;x \leq b)$$
* Value must lie **inside** the range between *a* and *b*, **excluding** *a* and **including** *b*.

* *Inclusive-Exclusive*
$$(a \leq x;\;x < b)$$
* Value must lie **inside** the range between *a* and *b*, **including** *a* and **excluding** *b*.

* *Exclusive-Exclusive*
$$(a < x;\;x < b)$$
* Value must lie **inside** the range between *a* and *b*, **excluding both** *a* and *b*.

**Exterior (Disjunction)**:

- *Inclusive-Inclusive*
$$(x \leq a;\;x \geq b)$$
* Value must lie **outside** the range between *a* and *b*, **including both** *a* and *b*.

* *Exclusive-Inclusive*
$$(x < a;\;x \geq b)$$
* Value must lie **outside** the range between *a* and *b*, **excluding** *a* and **including** *b*.

* *Inclusive-Exclusive*
$$(x \leq a;\;x > b)$$
* Value must lie **outside** the range between *a* and *b*, **including** *a* and **excluding** *b*.

* *Exclusive-Exclusive*
$$(x < a;\;x > b)$$
*  Value must lie **outside** the range between *a* and *b*, **excluding both** *a* and *b*.


