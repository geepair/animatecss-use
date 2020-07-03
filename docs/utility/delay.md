# 延迟动画

> [!NOTE|label:注意]
>
> `V3.x`版本全部不适用

### delay

| <p class="animated">delay-2s</p> | <p class="animated">delay-3s</p> |
| :------------------------------: | :------------------------------: |
| <p class="animated">delay-4s</p> | <p class="animated">delay-5s</p> |

<button id="callFunc">触发延迟动画</button>

> [!TIP|style:flat|label:Code]
>
> ~~<span class="tip">Old</span>（不适用）~~
>
> ```html
> <p class="animated bounce delay-2s">delay-2s</p>
> <p class="animated bounce delay-3s">delay-3s</p>
> <p class="animated bounce delay-4s">delay-4s</p>
> <p class="animated bounce delay-5s">delay-5s</p>
> ```
> <span class="tip">New</span>
> 
> ```html
> <p class="animate__animated animate__bounce animate__delay-2s">delay-2s</p>
> <p class="animate__animated animate__bounce animate__delay-3s">delay-3s</p>
> <p class="animate__animated animate__bounce animate__delay-4s">delay-4s</p>
> <p class="animate__animated animate__bounce animate__delay-5s">delay-5s</p>
> ```

<script>
    document.getElementById('callFunc').addEventListener('click', ()=>{
        let anim = document.getElementsByClassName('animated')
        for(let i = 0; i < anim.length; i++) {
            anim[i].classList.add('bounce', anim[i].innerText)
            anim[i].addEventListener('animationend', ()=>{
                anim[i].classList.remove('bounce', anim[i].innerText)
            })
        }
    })
</script>