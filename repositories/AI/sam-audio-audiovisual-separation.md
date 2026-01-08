# SAM-Audio — audiovisual source separation (Meta, CC-BY-NC)

**Type:** repository

**Summary:** SAM-Audio (Meta) is an open-source audiovisual source-separation project that extracts sound from a selected region in video using a PE-AV encoder and a flow-matching diffusion transformer.

**Tags:** #audio-separation #multimodal #source-separation #open-source

## Links

- https://ai.meta.com/blog/sam-audio/
- https://ai.meta.com/samaudio/
- https://github.com/facebookresearch/sam-audio

## Original Message

SAM-Audio: находка для шпиона

Meta продолжает расширять возможности SAM (Segment Anything Model), и теперь туда добавилась аудиомодальность. 

Выделяешь объект на видео и получаешь звук, который исходит исключительно из этой точки. Как вы понимаете, это просто находка для шпиона, ведь можно выделить диалог двух людей на видео и слышать только его, отделив от всего остального шума. Какие у этого другие применения — думайте сами. А так проект выглядит довольно интересно.

В основе лежит Perception Encoder Audiovisual (PE-AV), который выступает в роли ушей системы. Сама же архитектура построена на flow-matching diffusion transformer, который принимает на вход аудиомикс и промпт, а на выходе генерирует целевой и остаточный аудиотреки.

Модель умеет отделять звук по трём типам промптов, которые можно комбинировать. Это текстовый, визуальный (клик на объект в видео), span prompting (выделение временного отрезка, когда появляется звук). Но вот выделить что-то совсем похожее пока не удастся, например, одного певца из хора вырезать не получится.

При этом модель работает быстрее реального времени (RTF ≈ 0.7) и скейлится от 500M до 3B параметров. 

Веса и код выложены в опенсорс, но под некоммерческой лицензией (CC-BY-NC 4.0).

[Блогпост](https://ai.meta.com/blog/sam-audio/)
[Демо](https://ai.meta.com/samaudio/)
[GitHub](https://github.com/facebookresearch/sam-audio)

@ai_newz

---
*Saved from Telegram on 2026-01-08*
