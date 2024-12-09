# PREDICT: Multi-Agent-based Debate Simulation for Generalized Hate Speech Detection ([English](#english-version) | [Chinese](#中文版))

source: [paper](https://aclanthology.org/2024.emnlp-main.1166/) | [github](https://github.com/Hanyang-HCC-Lab/PREDICT)

## English Version

### Problem
The paper addresses the challenge of generalization in hate speech detection models caused by the differences in labeling criteria across public benchmarks. These discrepancies limit the ability of models to perform effectively on datasets with varied definitions of hate speech.

### Solution
The authors propose **PREDICT**, a multi-agent-based framework for hate speech detection that integrates diverse perspectives through debate simulation. PREDICT consists of two key phases:
1. **PRE (Perspective-based REasoning):** Each agent is assigned an independent perspective based on the labeling criteria of a specific dataset, generating stances and reasons for classification.
2. **DICT (Debate using InCongruenT references):** Agents representing opposing stances (hate and non-hate) debate using their references. A judge agent then classifies the input text and provides a balanced reason.

The framework leverages the concept of pluralism to respect diverse labeling criteria and mediates disagreements to reach a consensus.

### Results
PREDICT demonstrated superior generalization performance compared to baseline methods (e.g., majority voting) on five public benchmarks. Key results include:
- Enhanced accuracy in cross-dataset evaluations by integrating diverse perspectives.
- Effective mediation of disagreements between agents, with minority opinions incorporated during the debate simulation.
- Reduced reliance on dataset-specific biases, improving the framework’s applicability to diverse datasets.

### Observations
- **Key innovation:** The use of multi-agent debate simulations for hate speech detection is novel. As the authors state, “PREDICT respects diverse perspectives on hate speech and stores them as a reference for debate.”
- **Performance gains:** The paper reports that PREDICT consistently outperforms majority voting methods and dataset-specific models, particularly when handling datasets with varying definitions of hate speech.
- **Example of effective mediation:** The debate process ensures balanced decision-making by revising or extending arguments based on counterpoints from opposing stances.

### Conclusion
The PREDICT framework successfully addresses the generalization challenge in hate speech detection by integrating diverse perspectives through structured debate simulations. The study highlights the importance of pluralism in resolving conflicts arising from varied labeling criteria and opens avenues for applying multi-agent systems in broader social science research domains. However, further improvements in handling complex debates and reducing LLM biases are necessary for real-world deployment.

---

## 中文版本

### 問題
本論文針對現有仇恨言論檢測模型的泛化問題進行研究。由於不同公開數據集的標註標準存在差異，導致模型在處理不同數據集時性能不穩定，限制了其應用範圍。

### 解決方案
作者提出了一種名為 **PREDICT** 的新框架，通過多代理的辯論模擬來進行仇恨言論檢測。框架包括兩個主要階段：
1. **PRE (Perspective-based REasoning, 基於視角的推理)：** 為每個代理分配基於特定數據集標註標準的獨立視角，並生成對輸入文本的立場（hate 或 non-hate）及其理由。
2. **DICT (Debate using InCongruenT references, 基於不一致參考的辯論)：** 代理分為支持 hate 和 non-hate 的兩方進行辯論，最終由一個裁判代理根據辯論歷史給出最終的分類結果及平衡的理由。

該框架利用多元主義的理念，尊重數據集中不同的標註標準，並通過模擬辯論達成共識。

### 結果
PREDICT 在五個公開數據集上的實驗結果顯示，該框架的泛化能力優於基線方法（如多數投票）。關鍵結果如下：
- 在跨數據集評估中表現優異，能夠有效整合多種視角。
- 在代理觀點分歧時，PREDICT 能有效調解，並合理融入少數派觀點。
- 減少了對特定數據集偏差的依賴，提高了框架在不同場景下的適用性。

### 觀察
- **關鍵創新點：** 本文首創性地提出通過多代理辯論模擬進行仇恨言論檢測。正如作者所述：“PREDICT 尊重對仇恨言論的多樣化視角，並將其作為辯論參考保存。”
- **性能提升：** 論文報告顯示，PREDICT 的性能穩定優於多數投票方法及僅基於特定數據集的模型，特別是在標註標準存在差異的數據集上。
- **有效調解的案例：** 辯論過程通過對反對觀點的回應和修正，促進了平衡的決策。

### 結論
PREDICT 框架成功解決了仇恨言論檢測中的泛化挑戰。通過結構化的辯論模擬，該方法整合了多樣化的視角，並顯示出其在跨數據集應用中的優勢。本研究強調了多元主義在解決標註標準差異問題中的重要性，同時也為多代理系統在更廣泛的社會科學研究領域中的應用提供了可能。然而，仍需進一步改進框架在處理複雜辯論和減少大語言模型（LLM）偏見方面的能力，以實現實際應用的可行性。
