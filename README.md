مفاهیم و اصول اصلی کدنویسی تمیز با مثال

۱- خوانایی (Readability): کد باید به قدر کافی خواناتوس باشد. برنامه‌نویسان بیشتر از خواندن کد تا نوشتن آن درگیر هستند. کد خواناتوس، توجیه‌پذیر و مفهوم، برنامه‌نویسان دیگر را به‌سهولت به درک کد هدایت می‌کند.
# بد
x = "ThisIsAVariableThatStoresTheUserName"

# خوب
user_name = "JohnDoe"

------------------------------------------------------------


۲- نام‌گذاری مناسب (Meaningful Names): نام‌گذاری باید توصیفی و معنی‌دار باشد. نام متغیرها، توابع، کلاس‌ها و ... باید اطلاعات کافی را انتقال دهد تا برنامه‌نویسان دیگر بدون نگاه به جزئیات کد، بفهمند چه کاری انجام می‌شود.

// بد
function fn(x) {
  return x * 2;
}

// خوب
function calculateDouble(value) {
  return value * 2;
}

------------------------------------------------------------

۳- توابع کوچک (Small Functions): توابع باید اندازه‌ی کوچکی داشته باشند و یک کار خاص را انجام دهند. هر تابع باید تنها یک سطح انتزاع داشته باشد و وظیفه‌ی خاص خود را اجرا کند.

# بد
def process_data(data):
  # کد زیاد
  # ...
  # ...
  # ...
  return result

# خوب
def process_data(data):
  result = process_step1(data)
  result = process_step2(result)
  result = process_step3(result)
  return result

def process_step1(data):
  # کد مرتبط با مرحله ۱
  pass

def process_step2(data):
  # کد مرتبط با مرحله ۲
  pass

def process_step3(data):
  # کد مرتبط با مرحله ۳
  pass



------------------------------------------------------------


۴- یکسانی (Consistency): استفاده از یک الگو و یک استایل در کل کد به خوانایی و درک کد کمک می‌کند. کدهای یکسان به برنامه‌نویسان کمک می‌کنند تا الگوها و رفتارهای مشابه را تشخیص دهند.

// بد
function calculateArea(length, width) {
  // کد محاسبه مساحت
}

// خوب
function calculateRectangleArea(length, width) {
  // کد محاسبه مساحت
}


------------------------------------------------------------


۵- مسئولیت یکتا (Single Responsibility Principle - SRP): هر کلاس یا تابع باید مسئولیت یکتایی داشته باشد. این اصل از SOLID principles گرفته شده است.

# بد
class User:
  def process_data(self, data):
    # کد پردازش داده
    pass

# خوب
class DataProcessor:
  def process_data(self, data):
    # کد پردازش داده
    pass




------------------------------------------------------------


۶- نبايد اطلاعات داخلي را باز كرد (Encapsulation): کلاس‌ها باید جزئیات داخلی خود را پنهان کنند و تنها واسطه‌های لازم را ارائه دهند.

// بد
class BankAccount:
  def __init__(self, balance):
    self._balance = balance

# خوب
class BankAccount:
  def __init__(self, balance):
    self.balance = balance

------------------------------------------------------------


۷- کد تکراری (DRY - Don't Repeat Yourself): اصل DRY تکرار کد را کاهش داده و از استفاده‌های تکراری جلوگیری می‌کند. اگر یک قطعه کد در چندین جای کد تکرار شده باشد، باید آن قطعه را در یک مکان مشخص قرار داد.


// بد
function calculateRectangleArea(length, width) {
  return length * width;
}

function calculateSquareArea(side) {
  return side * side;
}

// خوب
function calculateArea(length, width) {
  return length * width;
}


------------------------------------------------------------


۸- تست پذیری (Testability): کد باید به‌سهولت تست‌پذیر باشد. این به‌معنای طراحی به‌گونه‌ای است که بتواند به‌سهولت تست شود و خطاها به‌راحتی شناسایی شوند.


# بد
def calculate_area(length, width):
  # کد محاسبه مساحت
  pass

# خوب
def calculate_area(length, width):
  # کد محاسبه مساحت
  pass

def test_calculate_area():
  # تست محاسبه مساحت
  pass


------------------------------------------------------------


۹- نگاه به جلو (Forward Looking): طراحی کد باید به آینده نیز نگاه کند. باید قابلیت توسعه و افزودن ویژگی‌های جدید را داشته باشد.

// بد
function calculate_discount(price, discount_rate):
  # کد محاسبه تخفیف
  pass

// خوب
function calculate_discount(price, discount_rate, additional_discount):
  # کد محاسبه تخفیف
  pass


------------------------------------------------------------


۱۰- تفکر نهایی (Ultimate Simplicity): کد باید به حداقل سادگی و پیچیدگی رسانده شود. اصول KISS (Keep It Simple, Stupid) و YAGNI (You Ain't Gonna Need It) در این‌جا مورد تأکید قرار می‌گیرند.


# بد
def complicated_algorithm(x, y, z):
  # کد پیچیده و سخت
  pass

# خوب
def simple_algorithm(x, y):
  # کد ساده و قابل فهم
  pass
