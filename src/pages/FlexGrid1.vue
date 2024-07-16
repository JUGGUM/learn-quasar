<template>
  <q-page class='q-pa-xl'>
    <section class='q-mb-xl'>
      <div class='text-h4 text-bold flex flex-center'>Flexbox - Gutter</div>
      <q-separator class='q-my-md' />
      <div class='bg-yellow'>
        <div class='q-gutter-x-md'>
          <div v-for="n in 4" :key="n" class='square'></div>
        </div>
        <div class='q-gutter-y-md'>
          <div v-for="n in 4" :key="n" class='bg-primary'>{{n}}</div>
        </div>
      </div>
      <q-separator spaced />
      <div class='bg-yellow'>
        <div class='row q-col-gutter-md'>
          <div v-for='n in 8' :key='n' class='col-12 col-sm-6 col-md-4 col-lg-3'>
            <q-card class='my-card'>
              <q-img src = "https://cdn.quasar.dev/img/parallax2.jpg">
                <div class='absolute-bottom text-subtitle2 text-center'>
                  Title
                </div>
              </q-img>
            </q-card>
          </div>
        </div>
      </div>
    </section>
    <section class='q-mb-xl'>
      <div class='text-h4 text-bold flex flex-center'>Flexbox - Col</div>
      <q-separator class='q-my-md' />
      <div class='row'>
        <div class='border col-2'>col-2</div>
        <div class='border col-8'>col-8</div>
        <div class='border col-2'>col-2</div>
        <div class='border col-2'>col-2</div>
      </div>
      <q-separator spaced />
      <div class='row'>
        <div class='border col'>col</div>
        <div class='border col'>col</div>
        <div class='border col'>col</div>
        <div class='border col'>col</div>
      </div>
      <q-separator spaced />
      <div class='row'>
        <div class='border col-auto'>col</div> <!--col-auto 문자열너비만큼차지-->
        <div class='border col'>col</div>
        <div class='border col'>col</div>
        <div class='border col'>col</div>
      </div>
      <q-separator spaced />
      <div class='row'>
        <div class='border col-grow'>col</div> <!--col-grow 나머지 너비만큼 차지-->
        <div class='border col-1'>col</div>
        <div class='border col-1'>col</div>
        <div class='border col-1'>col</div>
      </div>
      <q-separator spaced />
      <div class='row no-wrap'>
        <div class='border col-auto'>col-auto col-auto col-auto col-auto</div>
        <div class='border col-shrink'>col-shrink col-shrink col-shrink col-shrink</div>
        <!--col-shrink 컨테이너너비에따라서 자동으로 줄어든다-->
        <div class='border col-1'>col</div>
        <div class='border col-1'>col</div>
        <div class='border col-1'>col</div>
        <div class='border col-1'>col</div>
        <div class='border col-1'>col</div>
      </div>
    </section>
    <section class='q-mb-xl'>
      <div class='text-h4 text-bold flex flex-center'>Toolbar</div>
      <q-separator class='q-my-md' />
      <div class='row items-center justify-between bg-primary q-px-sm' :style="{minHeight :'50px'}">
        <div>
          <q-btn icon='menu' flat dense round color='white'/>
          <span class='text-h6 text-white-bold text-white'>Quasar App</span>
        </div>
        <q-btn icon='light_mode' flat dense round color='white'/>
      </div>
      <q-separator spaced/>
      <div class='row items-center justify-between bg-primary q-px-sm' :style="{minHeight :'50px'}">
          <q-btn icon='menu' flat dense round color='white'/>
          <span class='text-h6 text-white-bold text-white'>Quasar App</span>
        <q-btn icon='light_mode' flat dense round color='white'/>
      </div>
    </section>
    <section class='q-mb-xl'>
      <div class='text-h4 text-bold flex flex-center'>Flexbox - Row</div>
      <q-separator class='q-my-md' />
      <div class='row inline bg-yellow'>
        <div class='square'></div>
        <div class='square'></div>
        <div class='square'></div>
        <div class='square'></div>
        <div class='square'></div>
      </div>
      <q-separator spaced />
      <div class='row inline reverse bg-yellow'>
        <div v-for='n in 6' :key='n' class='square'>{{ n }}</div>
      </div>
      <q-separator spaced />
      <div class='row inline bg-yellow no-wrap'>
        <!-- flex방식으로 줄을바꿔 다음 행을 사용하지않고 옆으로뿌려줌 no-wrap -->
        <div v-for='n in 16' :key='n' class='square'>{{ n }}</div>
      </div>
    </section>
    <section class='q-mb-xl'>
      <div class='text-h4 text-bold flex flex-center'>Flexbox - Column</div>
      <q-separator class='q-my-md' />
      <div class='column inline bg-yellow'>
        <div class='square'></div>
        <div class='square'></div>
        <div class='square'></div>
        <div class='square'></div>
        <div class='square'></div>
      </div>
    </section>
  </q-page>
</template>

<script>
export default {};
</script>

<style lang='scss' scoped>
.square {
  height: 80px;
  width: 80px;
  background-color: $primary;
  border: 1px solid black;
  display: inline-block;
  font-weight: 900;
  color: white;
}
.border{
  border : 1px solid $primary;
  padding : 8px;
}
</style>
