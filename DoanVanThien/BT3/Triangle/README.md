BÁO CÁO BÀI TẬP TUẦN 5

Mô tả:

+ Chương trình viết bằng Java, test bằng JUnit
+ Chương trình là tìm số tam giác cân trong một mảng các đối tượng tam giác

Hàm cần kiểm thử:

public int total_isosceles_triangle(ArrayList<Triangle> arrayListTriangle) {
        if (arrayListTriangle.size() == 0) {
            return 0;
        }
        int index = 0;
        int length = arrayListTriangle.size();
        int total_isosceles_triangle = 0;
        while (index < length) {
            Triangle triangle = arrayListTriangle.get(index);
            int edge1 = triangle.getEdge1();
            int edge2 = triangle.getEdge2();
            int edge3 = triangle.getEdge3();
            if ((edge1 > 0 && edge2 > 0 && edge3 > 0) && ((edge1 + edge2 > edge3) && (edge1 + edge3 > edge2) && (edge3 + edge2 > edge1)) 
                    && ((edge1 == edge3) || (edge1 == edge2) || (edge3 == edge2))){
                total_isosceles_triangle += 1;
            }            
            index++;
        }
        return total_isosceles_triangle;
    }



