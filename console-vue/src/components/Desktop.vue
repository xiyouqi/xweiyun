<template>
  <div class="desktop">
    <div style="margin-bottom:15px;">
      <el-button type="primary">新建 <i class="el-icon-upload"></i></el-button>
    </div>
    <el-row :gutter="20">
      <el-col :span="4" :xs="8" v-for="res in resources" :key="res.node_id">
        <div class="grid-content bg-purple">
          <p>
            <img :src="'../../static/box-icons/' + res.node_type + '.png'">
          </p>
          <p>{{res.node_name}}</p>
          <el-button-group>
            <el-button type="text" icon="edit"></el-button>
            <el-button type="text" icon="share"></el-button>
            <el-button type="text" icon="delete"></el-button>
          </el-button-group>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'desktop',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      resources: [
        {
          node_id: '1',
          node_name: 'Base',
          node_type: 'folder-empty'
        },
        {
          node_id: '2',
          node_name: 'System',
          node_type: 'folder-empty'
        },
        {
          node_id: '3',
          node_name: 'WOM',
          node_type: 'app'
        },
        {
          node_id: '4',
          node_name: 'EAP',
          node_type: 'app'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.desktop {
  padding: 15px;
}

.el-row {
  margin-bottom: 20px;
  &:last-child {
    margin-bottom: 0;
  }
}

.grid-content {
  padding: 20px;
  text-align: center;
}

.grid-content .el-button-group {
  display: none;
}

.grid-content:hover {
  background-color: #D3DCE6;
  border-radius: 5px;
}

.grid-content:hover .el-button-group {
  display: inline-block;
}
</style>
