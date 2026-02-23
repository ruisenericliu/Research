How can one easily teach caption-pretrained VLMs the ability to localize objects? 🤔 We show that a small Positional Insert (PIN) can unlock object localization abilities without needing annotated data on frozen autoregressive VLMs.
 
Accepted to [#CVPR2024](https://www.linkedin.com/feed/hashtag/?keywords=cvpr2024&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7188438995876392960) and MMFM workshop.
 
📝: [https://lnkd.in/eXwYQxRb](https://lnkd.in/eXwYQxRb)  
🌐: [https://lnkd.in/edwQvtcA](https://lnkd.in/edwQvtcA)
 
🔍 We assess the localization capabilities of caption-pretrained VLMs and find that they cannot provide location information, often being "chatty". GPTV-4 can output a bounding box, though its pretraining details are undisclosed. Further analysis is available in the paper.
 
💡 We introduce PIN, a VLM PEFT method that slides into a frozen VLM to enable object localization. PIN is trained using a next-token text prediction task on synthetic data, without requiring new output heads.
 
📚 We demonstrate that adapting frozen VLMs does not require labeled data; instead, we use synthetic data where we overlay rendered objects at random locations on background images. This approach generates a self-supervising signal that we exploit to train the PIN module.
 
🚀 The PIN-enhanced VLM is able to localize objects in various settings and also for object classes not seen during the synthetic localization training.
 
Joint work with [Nimrod Barazani](https://www.linkedin.com/in/ACoAAB87xOkB4-4b8jj-Fsuq6LliSIVbPQ8-F-4), [Cees Snoek](https://www.linkedin.com/in/ACoAAADIsj8BAEDGRG789r2iYtd9ppSSKAvVK0s), [Yuki Asano](https://www.linkedin.com/in/ACoAABEqThIBEtXHRI5Ji7wMWamdW0qm2l2MVgk)  
[University of Amsterdam](https://www.linkedin.com/company/university-of-amsterdam/)
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>