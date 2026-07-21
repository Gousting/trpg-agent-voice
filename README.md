# TRPG Agent Voice

语音识别版 AI 跑团。用语音和 KP 互动，faster-whisper 做本地 STT，TTS 回话。目标是真人嘉宾无需打字就能参与跑团。

## 是什么

基于 [trpg-agent](https://github.com/Gousting/trpg-agent) 核心引擎的语音插件。你在麦克风前说话 → faster-whisper 转文字 → 注入当前玩家 prompt → KP 回应 → TTS 朗读。全程不需要碰键盘。

## 安装

```bash
pip install trpg-agent-voice
```

会自动安装 `trpg-agent[voice]`（含 faster-whisper）。

## 使用

```bash
trpg-voice
# 选择麦克风设备，开始语音跑团
```

## 技术栈

- faster-whisper（本地 STT，支持多语言，< 1s 延迟）
- edge-tts / Piper（TTS 回话，KP 旁白朗读）
- 与 trpg-agent 核心库共享 Session 和 LLM 层

## 当前状态

项目骨架已建立。语音采集和 STT 管道待实现。

## 许可证

MIT
