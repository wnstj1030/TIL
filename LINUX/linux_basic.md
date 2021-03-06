# **LINUX BASIC**
### **hello 디렉터리 생성**
![Untitled](../img/linux_1.png)

mkdir 명령어를 사용하여서 hello라는 디렉토리를 만들었다.

### **hello 디렉터리 안에 본인 이니셜 txt 파일 생성**
![Untitled](../img/linux_2.png)

vi 명령어를 사용해서 KJS.txt라는 텍스트파일을 만들었다.

### **본인 이니셜 txt 파일을 동일 디렉터리에 복사**
![Untitled](../img/linux_3.png)

cp명령어를 사용하여 KJS 텍스트파일을 hello 디렉토리에 복사하였다.

![Untitled](../img/linux_4.png)

파일의 내용을 보니 복사가 잘되었다.

<aside>
💡 디렉토리를 복사할때는 -r옵션을 추가 하여야한다. ex) cp -r directory directory_cp

<br>
</aside>

### **원본 파일을 삭제**

![Untitled](../img/linux_5.png)
rm -rf 명령어를 사용해서 원본파일(KJS.txt)를 삭제하였다.


### **복사본을 다른 디렉터리로 이동**

![Untitled](../img/linux_6.png)

파일을 옮기기위해서 먼저 kim 디렉토리를 만든 후 pwd명령어로 kim 디렉토리의 절대주소를 찾았다.

![Untitled](../img/linux_7.png)

이제 다시 hello 디렉토리에 들어가서 KTS.txt_cp 파일을 옮기는 과정을 하였다.

<aside>
💡 mv directory 옮기려는 곳의 절대주소

</aside>

<br>위 명령어를 사용하여 KJS.txt_cp파일을 kim디렉토리의 절대주소를 이용하여 kim 디렉토리로 파일을 옮겼다.

ls 명령어로 확인해보니 잘 이동되었다!

### **hello 디렉터리 삭제**

![Untitled](../img/linux_8.png)
hello 디렉토리를 삭제하기 위해 일단 ls -al 명령어로 디렉토리를 확인한후

rmdir 명령어를 사용해서 rmdir hello를 입력한후 ls -al로 확인한 결과 hello 디렉토리가 삭제되었다.

### **cat 명령어 사용해서 file_1, file_2 생성**

![Untitled](../img/linux_9.png)
cat >을 이용하여 file_1,file_2를 만들었고,

*cat > file_1 한 후 내용을 적은뒤 crtl + d를 누르면 작성이 완료된다.

ls -al로 확인해보니 제대로 생성되었다

### **file_1내용을 file_2에도 작성해보기**
![Untitled](../img/linux_10.png)

먼저 file_1에 kimjunseo라는 내용을 입력했고, car > 을 사용해서

kimjunseo라는 내용을 file_2에도 입력했고, cat으로 확인하였다.

### **file_2에 다른 문장 덮어쓰기**

![Untitled](../img/linux_11.png)
<aside>
💡 cat > 은 원래 있던 내용위에 덮어쓸때 사용하고, cat >> 은 원래 있던 내용에 추가해서 적을때 사용한다.

</aside>

위에 내용에 따라서 file_2에 다른 문장을 덮어쓰기를 하기 위해 cat > 사용하여 Junseo라는 내용으로 덮어썼다.

### **file_1의 앞 3문장 출력**
![Untitled](../img/linux_12.png)

일단 여러줄을 출력하기 위해서 file_1, file_2에 각각 여러줄의 내용을 넣어주었다.

이제 file_1의 앞 3문장을 출력하기 위해서 head 명령어를 사용해야된다.

<aside>
💡 head 파일이름 -n num → 파일의 앞에서부터 num개의 문장을 출력한다.

</aside>

![Untitled](../img/linux_13.png)

따라서 file_1의 앞 3문장을 출력하기 위해 head file_1 -n 3을 써주었다.

### **file_2의 뒷 4문장 출력**

파일의 앞쪽부터 몇문장을 출력하기 위해서는 head를 써주었지만

파일의 뒷 몇문장을 출력하기 위해서는 tail 이라는 명령어가 필요하다

tail 명령어는 head 명령어와 동일하게 사용하면된다.
![Untitled](../img/linux_14.png)
따라서 결과는 이렇게 출력된다.
### **file_1의 group 권한을 r—로 변경해보기**
![Untitled](../img/linux_15.png)
-/rw-/rw-/r— 에서 그룹의 권한은 2번째로 rw-이고, 읽기와 쓰기권한이 있다.

이제 이 권한을 읽기 권한만 있게 바꿔주면 된다. 

권한을 변경하기 위해서는 chomd라는 명령어가 필요하다.

<aside>
💡 r w x는 각각 2진수로 4 2 1 값으로 되어있다.

</aside>

<aside>
💡 chmod 644 file_1 → 이렇게 쓰면 된다.

</aside>

![Untitled](../img/linux_16.png)

chmod 명령어를 입력후 권한을 봐보면 rw- → r—로 바뀌었다.

### **vi 에디터를 이용하여 파일 생성(apple.txt)**
![Untitled](../img/linux_17.png)
vi apple.txt를 사용하여 파일을 생성하였다.

### **apple.txt 파일에 아무 문구나 15줄 입력하고 저장한 후, cat 명령어로 출력**
![Untitled](../img/linux_18.png)
아무문구나 15줄 적었고 esc를 누른뒤 :wq는 저장하고 종료한다는 뜻으로 사용했고,

cat으로 파일을 출력하면 된다.

![Untitled](../img/linux_19.png)
