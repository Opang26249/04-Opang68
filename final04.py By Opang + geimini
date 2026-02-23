import time
import random

def play_game():
    print("-------------------------------------------------------")
    print("สวัสดี! ยินดีต้อนรับสู่เกมทายตัวเลข 1 - 10 [ฺBy นายฐานพัฒณ์ พับขุนทด_4/4_04]")
    print("-------------------------------------------------------")
    time.sleep(1)
    
    user_name = input("ก่อนจะเริ่ม นายชื่ออะไรหรอ? : ")
    print(f"โอ้ชื่อ {user_name} ฟังดูเท่และฉลาดมากเลยนะ!")
    time.sleep(1.5)
    
    while True: # ลูปหลักเพื่อให้เล่นซ้ำได้หลายรอบ
        print(f"\nเอาล่ะ {user_name} ฉันสุ่มเลข 1 ถึง 10 ไว้ในใจ...")
        random_number = random.randint(1, 10)
        attempts = 0
        max_attempts = 5 # กำหนดจำนวนครั้งที่ทายได้
        
        print(f"นายมีโอกาสทาย {max_attempts} ครั้งนะ เริ่มได้!")
        
        while attempts < max_attempts:
            try:
                guess = int(input(f"ครั้งที่ {attempts + 1} | ป้อนตัวเลข: "))
            except ValueError:
                print("⚠️ แย่ละ! พิมพ์เฉพาะตัวเลขสิเพื่อน")
                continue
            
            attempts += 1
            
            if guess < random_number:
                print("🔼 น้อยไปหน่อย! ลองเลขที่มากกว่านี้ดู")
            elif guess > random_number:
                print("🔽 มากไปแล้ว! ลองเลขที่น้อยกว่านี้หน่อย")
            else:
                print(f"🎉 สุดยอดไปเลย {user_name}! นายทายถูกใน {attempts} ครั้ง!")
                break
            
            if attempts == max_attempts:
                print(f"😱 ว้า... หมดสิทธิ์ทายแล้ว เฉลยคือ {random_number} ไว้คราวหน้าเอาใหม่นะ!")

        # ถามว่าอยากเล่นอีกไหม
        play_again = input("\nอยากลองอีกสักตั้งไหม? (พิมพ์ y เพื่อเล่นต่อ / พิมพ์ n เพื่อเลิก): ").lower()
        if play_again != 'y':
            print(f"ขอบคุณที่มาเล่นนะ {user_name} บ๊ายบาย!")
            break

if __name__ == "__main__":
    play_game()
