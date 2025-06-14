# Cucumber-Testing-TE

## Setup Project

1. **Clone repository dari GitHub:**
    ```bash
    git clone https://github.com/Im-A-Nuel/Cucumber-Testing-TE.git
    
    cd <nama-folder-project>
    ```

2. **Buka terminal** dan pastikan Node.js sudah terinstall:
    ```bash
    node -v
    npm -v
    ```
3. **Jalankan perintah berikut di terminal/CMD untuk menginstall dependencies:**
    ```bash
    npm install
    ```

---

## Fitur: Order and Cart

### 1. Failed login with invalid credential
```gherkin
Scenario: Failed login with invalid credential
    Given the user is on the login page
    When the user enters an invalid username and password
    And the user clicks the login button
    Then the user should see a failed message
```

### 2. Successfully adding an item to cart
```gherkin
Scenario: Successfully adding an item to cart
    Given the user is on the login page
    And the user is on the item page
    When the user add item to the cart
    And the user in the item list
    Then item should be seen in the item page
```

### 3. Successfully removing an item from cart
```gherkin
  Scenario: Successfully removing an item from cart
    Given the user is on the login page
    And the user is on the item page
    When the user add item to the cart
    And the user in the item list
    When the user remove item to the cart
    Then item shouldn't be seen in the item page
```

### 4. Checkout process with empty cart
```gherkin
  Scenario: Checkout process with empty cart
    Given the user is on the login page
    And the user is on the cart page
    When the user tries to checkout
    Then the user should see a message "Cart is empty"
```

### 5. Logout after successful login
```gherkin
  Scenario: Logout after successful login
    Given the user is on the login page
    When the user enters a valid username and password
    And the user clicks the login button
    Then the user should see the home page
    When the user clicks the logout button
    Then the user should be redirected to the login page
```
---

## Cara Menjalankan Test
* **Pastikan anda memiliki browser Chrome**

* **Jalankan perintah berikut di terminal/CMD :**
    ```bash
    npm test
    ```


## Hasil Testing
![alt text](image.png)