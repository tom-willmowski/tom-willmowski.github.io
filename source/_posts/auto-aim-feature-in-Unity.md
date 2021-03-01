---
title: mechanika auto-aim w Unity
date: 2020-08-29 13:33:34
tags:
---
Jak powinien wygladac post?

```c#
private void Start()
{
    for(int i=0; i<count; i++)
    {
        Zombie zombie = Instantiate(prefab);
        zombie.name = $"zombie {i}";
        MaterialPropertyBlock block = new MaterialPropertyBlock();
        Color randomColor = GenerateColor();
        block.SetColor("_SecondaryColor", randomColor);
        zombie.GetComponent<Renderer>().SetPropertyBlock(block);
        zombies.Add(((Color32)randomColor).ToString(), zombie);
    }
}
```