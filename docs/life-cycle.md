# 视频生成任务API

## 获取任务列表

GET /task

## 创建视频生成任务

POST /task

## 获取视频生成状态

GET /task/{task_id}

## 视频摘要

获取: GET /task/{task_id}/summary
编辑: POST /task/{task_id}/summary

请注意本操作会更新tts结果, 所以可能会有1分钟左右的response时间, 更新完摘要后timeline会有改变, 请再次请求/task/{task_id}/timeline来获取最新timeline.

## 视频时间轴

请注意, 此json中client需要关心的就是schema中列出来的字段. 在tracks中有type为'audio'的, 请勿更改他们在列表中的顺序. 调整素材顺序的话请只调整type为'video'和'image'的track.

获取: GET /task/{task_id}/timeline
编辑: POST /task/{task_id}/timeline
