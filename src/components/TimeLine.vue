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
                  {{item.time}}
              </div>
              <i></i>
          </span>
          <article>
                <div class="hospital">
                    <span>{{item.hospital}}</span><span>{{item.medicalType}}</span><span>{{item.code}}</span>
                </div>
                <div>
                    <span>入院诊断</span>
                    <span>{{item.Diagnosis}}</span>
                </div>
                <div>
                    <span>入院诊断</span>
                    <span>{{item.Diagnosis}}</span>
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
    @base: blue;
    #timeLine {
      display: flex;
      flex-direction: column;
      p {
          font-size: 16px;
      }
      section {
          display: flex;
          flex-direction: row;
          align-items:flex-start;
          span {
              display: flex;
              flex-direction: row;
              align-items:center;
              .outCircle{
                  width: 16px;
                  height: 16px;
                  border-radius: 16px;
                  background-color: @base;
                  display: flex;
                  justify-content: center;
                  align-items:center;
                  position: relative;
                  .innerCircle {
                      width: 6px;
                      height: 6px;
                      background-color: @base;
                      border-radius: 6px;
                      border: 3px solid #fff;
                  }
              }
              .date {
                  margin-left: 15px;
                  font-size: 13px;
                  line-height: 16px;
                  font-weight: bold;
                  height: auto;
              }
              i {
                  width: 28px;
                  height: 28px;
                  background-color: #eee;
              }
          }
          article {
              display: flex;
              flex-direction: column;
              font-size: 13px;
              .hospital {
                span:first-child {
                  font-size: 16px
                }
              }
              div {
                  display: flex;
                  flex-direction: row;
              }
          }
      }
      section:before {
          content: '';
          position: relative;
          top: 0;
          left: 8px;
          height: 100%;
          width: 2px;
          background: @base;
          margin-top: 10px;
      }
      section:last-child:before {
          content: '';
          position: relative;
          top: 0;
          left: 8px;
          height: 0;
          width: 2px;
          background: none;
          margin-top: 10px;
      }
    }
</style>
