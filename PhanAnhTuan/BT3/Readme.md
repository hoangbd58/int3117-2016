BÁO CÁO BÀI TẬP TUẦN 7
Áp dụng tiêu chuẩn kiểm thử All-DU Path cho BT2 
1. Áp dụng cho biến nhansu
-  1->2->3->11                   
	+ Bộ kiểm thử
		nhansu[] = null
-  1->2->3->4->5->10->5
	+ Bộ kiểm thử
		nhansu= new NhanSu[3];
		nhansu[0] = new NhanSu(3,2.0);
        	nhansu[1] = new NhanSu(2,2.9);
        	nhansu[2] = new NhanSu(1,2.0);
2. Áp dụng cho biến nhansu[i].diemTrungBinh
- 1->2->3->4->5->6->10->5
	+ Bộ kiểm thử
		nhansu= new NhanSu[3];
		nhansu[0] = new NhanSu(3,-2.0);
        	nhansu[1] = new NhanSu(2,-2.9);
        	nhansu[2] = new NhanSu(1,-2.0);
- 1->2->3->4->5->6->7->9->10->5
	+ Bộ kiểm thử
		nhansu= new NhanSu[3];
		nhansu[0] = new NhanSu(3,3.1);
        	nhansu[1] = new NhanSu(2,3.);
        	nhansu[2] = new NhanSu(1,3.6);
- 1->2->3->4->5->6->7->8->9->10->5
	+ Bộ kiểm thử
		nhansu= new NhanSu[3];
		nhansu[0] = new NhanSu(1,2.6);
        	nhansu[1] = new NhanSu(2,2.3);
        	nhansu[2] = new NhanSu(3,2.7);

- 1->2->3->4->5->6->7->8->10->5
	+ Bộ kiểm thử
		nhansu= new NhanSu[3];
		nhansu[0] = new NhanSu(1,1.6);
        	nhansu[1] = new NhanSu(2,1.3);
        	nhansu[2] = new NhanSu(3,1.7);

3. Áp dụng cho biến nhansu[i].soNamKinhNghiem
- 1->2->3->4->5->6->10->5
	+ Bộ kiểm thử
		nhansu= new NhanSu[3];
		nhansu[0] = new NhanSu(-1,-2.0);
        	nhansu[1] = new NhanSu(-2,-2.9);
        	nhansu[2] = new NhanSu(-3,-2.0);

- 1->2->3->4->5->6->7->8->9->10->5
	+ Bộ kiểm thử
		nhansu= new NhanSu[3];
		nhansu[0] = new NhanSu(1,2.6);
        	nhansu[1] = new NhanSu(2,2.3);
        	nhansu[2] = new NhanSu(3,2.7);
3. Áp dụng cho biến dem
- 1->2->3->11
	+ Bộ kiểm thử
		nhansu[] = null
- 1->2->3->4->5->6->7->9->10->5->...->11
	+ Bộ kiểm thử
		nhansu= new NhanSu[3];
		nhansu[0] = new NhanSu(3,3.1);
        	nhansu[1] = new NhanSu(2,3.);
        	nhansu[2] = new NhanSu(1,3.6);
- 1->2->3->4->5->6->7->8->9->10->5->...->11
+ Bộ kiểm thử
		nhansu= new NhanSu[3];
		nhansu[0] = new NhanSu(1,2.6);
        	nhansu[1] = new NhanSu(2,2.3);
        	nhansu[2] = new NhanSu(3,2.7);
4.So sánh với MCDC
 - Độ phức tạp: cả 2 tiêu chuẩn đều tạo ra nhiều bộ kiểm thử. 
 - Thời gian tìm các trường hợp rẽ nhánh trong MCDC nhanh hơn so với tìm đường đi trong All-DU-Path.
 - Số ca kiểm thử: All-DU-Path nhiều hơn MCDC (11 so với 9).
 - Độ bao phủ: cả 2 tiêu chuẩn đều cho độ bao phủ bằng nhau.
5.Nhận xét
 - MCDC cho ít ca kiểm thử hơn và vẫn có độ bao phủ bằng All-DU-Path.
 - MCDC làm nhanh hơn so với All-DU-Path.
 - Một số trường hợp ALL-DU-Path có sự lặp lại đường đi qua các biến nên mất nhiều thời gian

