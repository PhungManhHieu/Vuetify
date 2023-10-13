<template>
    <v-layout class="rounded rounded-md">
        
            <v-app-bar title="Football News" color="teal-darken-4" image="https://picsum.photos/1920/1080?random">
                <template v-slot:image>
                    <v-img gradient="to top right, rgba(19,84,122,.8), rgba(128,208,199,.8)"></v-img>
                </template>

                <template v-slot:prepend>
                    <v-app-bar-nav-icon></v-app-bar-nav-icon>
                </template>

               

                <v-menu open-on-hover>
                    <template v-slot:activator="{ props }">
                        <v-btn color="yellow darken-2" dark v-bind="props"> NĂM HỌC </v-btn>
                    </template>

                    <v-list>
                        <v-list-item v-for="(item, index) in items" :key="index">
                            <v-list-item-title>{{ item.title }}</v-list-item-title>
                        </v-list-item>
                    </v-list>
                </v-menu>

                <v-spacer></v-spacer>

                <v-btn icon>
                    <v-icon>mdi-bell-outline</v-icon>
                </v-btn>

                <v-btn icon>
                    <v-icon>mdi-account</v-icon>
                </v-btn>

                <v-btn icon>
                    <v-icon>mdi-logout</v-icon>
                </v-btn>
            </v-app-bar>

            
            
        




        <v-navigation-drawer color="grey-darken-2" permanent name="drawer">
            <div class="d-flex justify-center align-center h-100">
                <v-card>
                    <v-layout>
                        <v-navigation-drawer image="https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg" permanent
                            theme="dark">
                            <v-list nav>
                                <v-list-item prepend-icon="mdi-newspaper" title="Quản lý Bài Viết"
                                    value="quanlybaiviet"></v-list-item>
                                <v-list-item prepend-icon="mdi-account-group" title="Danh Sách Người Đăng"
                                    value="qlDiem"></v-list-item>
                                <v-list-item prepend-icon="mdi-account-check" title="Kiểm Duyệt Viên"
                                    value="kiemduyetvien"></v-list-item>
                                <v-list-item prepend-icon="mdi-chart-bar" title="Thống kê" value="thongKe"></v-list-item>
                                <v-list-item prepend-icon="mdi-file-document" title="Báo cáo" value="baoCao"></v-list-item>
                                <v-list-item prepend-icon="mdi-printer" title="In ấn" value="inAn"></v-list-item>
                            </v-list>
                        </v-navigation-drawer>
                        <v-main style="height: 640px"></v-main>
                    </v-layout>
                </v-card>
            </div>
        </v-navigation-drawer>

        <v-main class="d-flex align-center justify-center" style="min-height: 300px;">
            Main Content
        </v-main>
    </v-layout>
</template>
<script>
export default {
  data: () => ({
    items: [
      { title: 'Click Me' },
      { title: 'Click Me' },
      { title: 'Click Me' },
      { title: 'Click Me 2' },
    ],
  }),
}
</script>