# AI数量限制
DefaultEngine.ini中有一个配置
[/Script/AIModule.CrowdManager]
MaxAgents=500

这个是注册怪物移动agent的最大数量限制，一定一定要比场景中怪物数量要多，否则个别怪物就不会移动.
