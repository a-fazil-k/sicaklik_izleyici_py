# ROS 2 Sıcaklık İzleyici Paketi (`sicaklik_izleyici_py`)

Bu depo, ROS 2 tabanlı iki düğümlü (`node`) bir sıcaklık izleme ve uyarı simülasyonu projesidir.

## Proje Yapısı ve Düğümler
* **`sensor.py`**: Rastgele/simüle edilmiş sıcaklık değerleri üreten ve `/sicaklik` konusuna (`topic`) veri yayınlayan (`publisher`) düğüm.
* **`izleyici.py`**: `/sicaklik` konusunu dinleyen (`subscriber`), sıcaklık değerlerini takip eden ve eşik değerin (30.0 °C) üzerine çıktığında uyarı veren düğüm[cite: 1].

## Kurulum ve Çalıştırma

1. Çalışma alanınıza gidin ve projeyi derleyin:
   ```bash
   colcon build --packages-select sicaklik_izleyici_py
   source install/setup.bash
