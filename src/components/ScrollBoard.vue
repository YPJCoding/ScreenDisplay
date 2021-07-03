<template>
  <div id="scroll-board">
    <dv-scroll-board :config="config" />
  </div>
</template>

<script>
export default {
  name: 'ScrollBoard',
  data () {
    return {
      config: {
        header: ['时间', '手机品牌', '数量', '平台'],
        data: [
          ['2021-07-01 19:25:00', '一加手机9 Pro', '5', '淘宝'],
          ['2021-07-02 17:25:00', 'OPPO Find X3 Pro', '13', '京东'],
          ['2021-07-03 16:25:00', 'vivo X60 Pro+', '6', '天猫'],
          ['2021-07-04 15:25:00', '一加手机9', '2', '拼多多'],
          ['2021-07-05 14:25:00', '小米11 Ultra', '1', '苏宁易购'],
          ['2021-07-06 13:25:00', '魅族18', '3', '国美'],
          ['2021-07-07 12:25:00', 'Redmi K40 Pro+', '4', '小米商城'],
          ['2021-07-08 11:25:00', '三星Galaxy S21 Ultra 5G', '2', '闲鱼'],
          ['2021-07-09 10:25:00', '小米10 至尊纪念版', '5', '京东到家'],
          ['2021-07-10 09:25:00', 'Redmi K30 至尊纪念版', '3', '转转']
        ],
        index: true,
        columnWidth: [50, 170, 230],
        align: ['center'],
        rowNum: 7,
        headerBGC: '#1981f6',
        headerHeight: 45,
        oddRowBGC: 'rgba(0, 44, 81, 0.8)',
        evenRowBGC: 'rgba(10, 29, 50, 0.8)'
      }
    }
  }
}
</script>

<style lang="less">
#scroll-board {
  width: 50%;
  box-sizing: border-box;
  margin-left: 20px;
  height: 100%;
  overflow: hidden;
}
</style>
