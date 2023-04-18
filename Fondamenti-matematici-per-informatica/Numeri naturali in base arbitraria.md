---
 Created: 2022-03-24 07:42
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Numeri naturali in base arbitraria
Sia $b \in \mathbb{N}$ diciamo che un [[Rappresentazione dei numeri naturali|numero naturale]] $n \in \mathbb{N}$ si può **rappresentare in base $b$** se $\exists k \in \mathbb{N}$ e $\epsilon_{0}, \epsilon_{1}, ..., \epsilon_{k} \in I_{b}= \{ 0, 1, ..., b-1 \}$ se $b \ge 1$ (altrimenti $I_{0} = p$) tale che $n = \epsilon_{0} b^{0}+ \epsilon_{1} b^{1} + ... + \epsilon_{k} b^{k}$ ossia:
$$n = \sum_{i = 0}^{k} \epsilon_{k} b^{k}$$