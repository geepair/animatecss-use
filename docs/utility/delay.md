# 延迟动画

### delay-2s

| <p class="animated">delay-2s</p> | <p class="animated">delay-3s</p> |
| :------------------------------: | :------------------------------: |
| <p class="animated">delay-4s</p> | <p class="animated">delay-5s</p> |

<button id="callFunc">延迟触发</button>

<script>
    let btn = document.getElementById('callFunc')
    let anim = document.getElementsByClassName('animated')
    btn.addEventListener('click', ()=>{
        for(let i = 0; i < anim.length; i++) {
            anim[i].classList.add('bounce', `delay-${i+2}s`)
            anim[i].addEventListener('animationend', ()=>{
                anim[i].classList.remove('bounce', `delay-${i+2}s`)
            })
        }
    })
   
</script>