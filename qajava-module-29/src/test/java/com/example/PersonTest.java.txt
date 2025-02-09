package com.example;

import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.*;

class PersonTest {

    @Test
    void testIsTeenagerTrue() {
        int age = 15;
        boolean result = Person.isTeenager(age);
        assertTrue(result);
    }

    @Test
    void testIsTeenagerFalse() {
        int age = 20;
        boolean result = Person.isTeenager(age);
        assertFalse(result);
    }

    // Дополнительный тест для проверки границ диапазона
    @Test
    void testBoundaryCases() {
        int age = 12;
        boolean result = Person.isTeenager(age);
        assertFalse(result);  // Ожидается false, но метод вернет true

        age = 19;
        result = Person.isTeenager(age);
        assertFalse(result);  // Ожидается false, но метод вернет true
    }
}
