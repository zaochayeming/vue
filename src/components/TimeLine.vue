<template>
  <div id="timeLine">
      <p>查看就诊记录</p>
      <section v-for="item in medicalRecords" :key="item">
          <span>
              <div class="outCircle">
                  <div class="innerCircle">
                  </div>
              </div>
              <div class="date">
                 <strong>{{item.time}}</strong>
              </div>
              <i></i>
          </span>
          <article>
                <div>
                    <strong>就诊医院</strong>{{item.hospital}}
                    <strong>医疗类型</strong>{{item.medicalType}}
                    <strong>就诊流水号</strong>{{item.code}}
                </div>
                <div>
                    <strong>入院诊断</strong>
                    {{item.Diagnosis}}
                </div>
                 <div>
                    <strong>入院诊断</strong>{{item.Diagnosis}}

                </div>
          </article>
      </section>
  </div>
</template>

<script>
export default {
  name: 'medicalRecords',
  data () {
    return {
    }
  },
  props: ['medicalRecords']
}
</script>

<style lang="less" scoped>
    @blue: #0888F2;
    @red: #FF4949;
    @base: #979797;
    #timeLine {
      display: flex;
      flex-direction: column;
      font-size: 13px;
      strong {
          margin: 0 40px 0 22px;
      }
      p {
          font-size: 16px;
      }
      section {
          display: flex;
          flex-direction: row;
          position: relative;
          align-items:flex-start;
          height: 100%;
          color: #4A5769;
          align-content: stretch;
          padding-bottom: 30px;
          span {
              display: flex;
              flex-direction: row;
              align-items:center;
              .outCircle{
                  width: 12px;
                  height: 12px;
                  border-radius: 12px;
                  background-color: @base;
                  display: flex;
                  justify-content: center;
                  align-items:center;
                  position: relative;
                  .innerCircle {
                      width: 6px;
                      height: 6px;
                      background-color: @blue;
                      border-radius: 6px;
                      border: 2px solid #fff;
                  }
              }
            //   .date {
            //       margin-left: 22px;
            //       line-height: 18px;
            //       height: auto;
            //       font-size: 14px;
            //   }
              i {
                  width: 28px;
                  height: 28px;
                  background-color: #eee;
              }
          }
          article {
              display: flex;
              flex-direction: column;
              div {
                  display: flex;
                  flex-direction: row;
                  line-height: 25px;
              }
          }
      }
      section:before {
          content: '';
          position: absolute;
          top: 0;
          left: 6px;
          height: 100%;
          width: 1px;
          background: @base;
          margin-top: 10px;
      }
      section:last-child:before {
          content: '';
          position: absolute;
          top: 0;
          left: 8px;
          height: 0;
          width: 1px;
          background: none;
          margin-top: 10px;
      }
    }
</style>
