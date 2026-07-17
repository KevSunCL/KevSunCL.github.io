## Sequential Contextual Fit Algorithm

![Sequential contextual fit algorithm](C:/Users/LENOVO/Downloads/contextual_fit_pilot/contextual_fit_algorithm_embedding_v4_linear_kernel.png)

The sequential contextual fit algorithm provides a general way to quantify how well a current information item fits its recent context. The core idea is simple: in any ordered stream of information, the current item is not processed in isolation, but relative to what has just occurred. A word is interpreted relative to preceding words, a decision is evaluated relative to recent choices and outcomes, an emotional state is shaped by its recent trajectory, and an action is understood relative to preceding movement states.

The algorithm first maps each item \(x_t\) into a domain-relevant vector representation \(\mathbf{z}_t=f(x_t)\). In language, this vector may be a word embedding; in visual processing, it may be an image or object embedding; in action analysis, it may be a sensor-window feature vector; in decision-making, it may encode choice, reward, and loss; and in emotion dynamics, it may represent valence and arousal. The current vector \(\mathbf{z}_t\) is then compared with the vectors of recent contextual items, such as \(\mathbf{z}_{t-1}\), \(\mathbf{z}_{t-2}\), and \(\mathbf{z}_{t-3}\).

The similarity between the current item and each contextual item is computed as:

\[
S(\mathbf{z}_t, \mathbf{z}_{t-j}).
\]

Because more recent information is usually more available or influential, the similarities are combined using a recency kernel. A simple linear kernel can be written as:

\[
K_{\mathrm{lag}} = 1 - \frac{\mathrm{lag}-1}{J},
\]

where \(J\) is the size of the context window. For \(J=3\), the weights for \(x_{t-3}\), \(x_{t-2}\), and \(x_{t-1}\) are \(1/3\), \(2/3\), and \(1\), respectively. The final contextual fit score is a normalized weighted average:

\[
\mathrm{Fit}(x_t)
=
\frac{
\sum_{j=1}^{J} K_j S(\mathbf{z}_t, \mathbf{z}_{t-j})
}{
\sum_{j=1}^{J} K_j
}.
\]

A high contextual fit score indicates that the current item is compatible with the recent context. A low score indicates that the current item departs from the recent context, suggesting possible processing difficulty, behavioral adjustment, or state transition.

This score can then be used as a predictor in regression models, mixed-effects models, or GAMMs:

\[
Y_{it}
=
s(\mathrm{Fit}_{it})
+
\mathrm{Controls}_{it}
+
\mathrm{RandomEffects}_{i}
+
\epsilon_{it}.
\]

The key question is whether contextual fit explains unique variance beyond established predictors in each domain.

### Application Scenarios

In language comprehension, the algorithm becomes a measure of semantic relevance. It can be used to predict reading time, eye movements, EEG responses such as N400 or P600, fMRI BOLD activity, and other indices of online language processing. A word that fits poorly with its local semantic context may require greater integration effort and therefore produce longer reading times or stronger neural responses.

In language production, the same principle may help explain speech duration, pause duration, typing time, and word selection difficulty. If an upcoming word fits well with the preceding semantic context, production may be more fluent; if it fits poorly, production may slow down.

In decision-making, contextual fit can be computed from recent choices, rewards, losses, and task states. A low fit score may indicate that the current decision state departs from recent decision history and may predict strategy shifts, choice switching, or exploratory behavior.

In emotion dynamics, each moment can be represented by valence-arousal states or affective features. Low contextual fit may indicate an emotional transition and may predict larger changes in subsequent affective ratings or physiological responses.

In action and behavior sequences, each movement window can be represented by sensor, pose, or activity features. Low contextual fit may signal that the current movement state is inconsistent with recent states and may therefore predict action transitions or behavioral state changes.

### Potential Impact

The potential value of this algorithm is that it offers a simple, interpretable, and cross-domain predictor of local context compatibility. Many sequence models aim to predict the next item, infer hidden states, or detect anomalies. By contrast, this metric asks a more explanatory question: how well does the current item fit the recently active context?

This makes the algorithm especially useful for cognitive, behavioral, and neural data analysis, where the goal is often not only prediction accuracy but also interpretable explanation. If contextual fit consistently predicts response times, neural activity, decision switching, affective change, or action transitions beyond domain-specific controls, it may provide a general framework for studying how systems process sequential information.

A cautious interpretation is that semantic relevance in language may be one special case of a broader sequential contextual-fit principle. In this broader view, low contextual fit reflects a local mismatch between the current information state and recent context, which may increase processing cost, promote behavioral adjustment, or mark the beginning of a state transition.