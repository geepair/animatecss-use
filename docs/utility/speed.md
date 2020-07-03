# 动画速度

> [!NOTE|label:注意]
>
> `V3.x`版本全部不适用

### speed

| <p class="animated">slower</p> | <p class="animated">slow</p> |
| :------------------------------: | :------------------------------: |
| <p class="animated">fast</p> | <p class="animated">faster</p> |

<button id="callFunc">触发动画速度</button>

> [!TIP|style:flat|label:Code]
>
> ~~<span class="tip">Old</span>（不适用）~~
>
> ```html
> <p class="animated bounce slow">slow</p>
> <p class="animated bounce slower">slower</p>
> <p class="animated bounce fast">fast</p>
> <p class="animated bounce faster">faster</p>
> ```
>
> <span class="tip">New</span>
> 
> ```html
> <p class="animate__animated animate__bounce animate__slow">slow</p>
> <p class="animate__animated animate__bounce animate__slower">slower</p>
> <p class="animate__animated animate__bounce animate__fast">fast</p>
> <p class="animate__animated animate__bounce animate__faster">faster</p>
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