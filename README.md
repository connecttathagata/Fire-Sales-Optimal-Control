# Fire-Sales-Optimal-Control

This is the code for the Optimal Control problem which arises when a bank is trying to minimize losses while liquidating assets to satisfy regulatory constraints. This is a multiasset generalization of Feinstein (2019) https://arxiv.org/pdf/1807.02711.pdf.

\begin{equation*}
\begin{aligned}
& {\text{min}}
& & \int_0^T \sum_{i=1}^m \gamma_i^2(t) dt \\
& \text{s.t.}
& & \dot{\Gamma}_i(t)=\gamma_i(t), \; i = 1, \ldots, m.\\
& {\text{}}
& & \dot{q}_i(t)=\dot{f_t^i}(t)f_{\Gamma_i}(\Gamma_i(t))+\dot{\Gamma}_i(t)f_t^i(t)\dot{f_{\Gamma_i}}(\Gamma_i(t)), \; i = 1, \ldots, m.\\
& {\text{}}
& & \sum_{i=1}^m \alpha_i \dot{\Psi}_i(t)=\\
& {\text{}}
& & \frac{[\sum_{i=1}^m (\alpha_i \theta_{min}-1)(s_i-\Gamma_i(t))q_i(t)][\sum_{i=1}^m \alpha_i(s_i-\Gamma_i(t))\dot{q}_i(t)]}{[\sum_{i=1}^m (\alpha_i \theta_{min}-1)(s_i-\Gamma_i(t))q_i(t)]}\\
& {\text{}}
& & \Gamma_i(t) \leq s_i, \; i = 1, \ldots, m.\\
& {\text{}}
& & \Gamma_i(0)=0, \; q_i(0)=1, \; i = 1, \ldots, m.
\end{aligned}
\end{equation*}
