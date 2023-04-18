---
 Created: 2022-05-11 13:46
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Covarianza
$$Cov(X, Y) = E((X - E(X))(Y - E(Y))) = E(XY - E(X)Y - XE(Y) + E(X)E(Y)) = E(XY) - E(X)E(Y)$$
$$Cov(X, X) = Var(X) = E(X^{2}) - E(X)^{2}$$
$$Cov(aX + b, cY + d) = E((aX + b - E(aX + b))(cY + d - E(cY + d))) = acE((X - E(X))(Y - E(Y))) = acCov(X, Y)$$