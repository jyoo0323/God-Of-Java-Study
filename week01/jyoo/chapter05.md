# Ch.05 계산을 하고 싶어요
- `직접해 봅시다`
  ```java
    public class OperatorCompound {
        public static main(String[] args) {
            OperatorCompound oc = new OperatorCompound();
            oc.compound();
        } 
        public void compound() {
            int intValue = 10;
           intValue+=5;
            System.out.println(intValue);
            intValue-=5;
            System.out.println(intValue);
            intValue*=5;
            System.out.println(intValue);
            intValue/=5;
            System.out.println(intValue);
            intValue%=5;
            System.out.println(intValue);
        }
    }
  ```
- 자바의 유일한 예약어로 되어 있는 연산자 == instanceof
    - 10장에서 제대로 설명을 할 것이라고 함
- `직접해 봅시다`
  ```java
  public class SalaryManager {
    public static void main(String[] args) {
        SalaryManager sm = new SalaryManager();
        double monthlySalary = sm.getMonthlySalary(20000000);
        System.out.println("monthlySalary = " + monthlySalary);
  
        boolean over200 = monthlySalary <= 2000000;
        System.out.println("over200 = " + over200);
    }
  
    public double getMonthlySalary(int yearlySalary) {
        double monthlySalary = yearlySalary / 12.0;
        double taxes = calculateTax(monthlySalary) + calculateNationalPension(monthlySalary)
            + calculateHealthInsurance(monthlySalary);
        monthlySalary -= taxes;
        return monthlySalary;
    }
  
    public double calculateTax(double monthlySalary) {
        return monthlySalary * 0.125;
    }
  
    private double calculateHealthInsurance(double monthlySalary) {
        return monthlySalary * 0.135;
    }
  
    private double calculateNationalPension(double monthlySalary) {
        return monthlySalary * 0.081;
     }
  }
  ```

- `정리해 봅시다`
    - 값을 할당할 때 사용하는 연산자의 기호는 무엇인가요?
        - =
    - 기본적인 덧셈, 뺄셈, 곱셈, 나눗셈, 나머지를 계산할 때 사용하는 연산자의 기호는 순서대로 각각 무엇인가요?
        - +,-,*,/
    - += 는 무엇을 할 때 사용하는 연산자 인가요?
        - 어떤 변수에 후열로 오는 숫자값을 더할때
    - 연산의 순서를 모르거나 확실히 하고 싶을 때에는 어떤 기호를 사용해야 하나요?
        - () 소괄호
    - ==와 !=의 차이는 무엇인가요?
        - 같냐 다르냐
    - <와 <=의 차이는 무엇인가요?
        - 같거나 크다와 큰가의 차이로, 왼쪽 값이 오른쪽값과 비교해 초과하는지 이상인지의 차이
    - ! 연산자는 어떤 타입에 사용 할 수 있나요?
        - boolean
    - ? : 로 표시하는 삼항 연산자의 ?와 : 뒤에 명시해 주는 값은 무엇을 의미 하나요?
        - ? 앞의 값이 true 일 때 ? 뒤에 값을 할당하고, false 일 경우 : 뒤의 값을 할당
    - 자바는 형변환을 한다고 했는데, short의 값을 long에 할당할 때에는 어떤 것을 해 주어야 하나요?
        - upcasting
    - 반대로 long값을 short에 할당할 때에는 어떤 것을 해 주어야 하나요?
        - downcasting
    - 위의 두 문제에서 어떤 경우가 기존 값이 사라지고, 엉뚱한 값으로 바뀔 수 있나요?
        - downcasting