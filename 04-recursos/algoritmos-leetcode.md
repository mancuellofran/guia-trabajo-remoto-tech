# 🧮 Algoritmos y LeetCode para Entrevistas Técnicas

> **Domina la resolución de problemas algorítmicos y prepárate para cualquier entrevista técnica con esta guía completa.**

## 🎯 ¿Por qué son Importantes los Algoritmos?

- **85%** de las entrevistas técnicas incluyen problemas algorítmicos
- **90%** de las empresas FAANG evalúan habilidades de programación
- **80%** de los desarrolladores fallan en la primera entrevista técnica
- Son la **base** para resolver problemas complejos en el trabajo real

## 📊 Estructura de Entrevista Técnica

### 1. **Warm-up** (5-10 minutos)
- Preguntas básicas de programación
- Validación de sintaxis
- Comprensión del problema

### 2. **Problema Principal** (30-45 minutos)
- Algoritmo de complejidad media-alta
- Optimización y análisis de complejidad
- Testing y casos edge

### 3. **Follow-up** (10-15 minutos)
- Variaciones del problema
- Optimizaciones adicionales
- Preguntas de escalabilidad

## 🎯 Estrategia de Resolución (CLEAR)

### C - **Clarify** (Clarificar)
- Entender el problema completamente
- Hacer preguntas sobre casos edge
- Confirmar inputs y outputs esperados

### L - **Examples** (Ejemplos)
- Crear ejemplos con inputs pequeños
- Verificar la lógica paso a paso
- Identificar patrones

### E - **Approach** (Enfoque)
- Explicar la estrategia general
- Considerar diferentes algoritmos
- Elegir la mejor opción

### A - **Code** (Código)
- Implementar la solución
- Código limpio y legible
- Comentarios cuando sea necesario

### R - **Review** (Revisar)
- Verificar la lógica
- Probar con casos edge
- Analizar complejidad temporal y espacial

## 📚 Patrones Algorítmicos Esenciales

### 1. Two Pointers
**Cuándo usar**: Arrays ordenados, palíndromos, sumas
**Complejidad**: O(n)
**Ejemplos**: Two Sum, Valid Palindrome, Container With Most Water

```javascript
// Ejemplo: Two Sum en array ordenado
function twoSum(nums, target) {
    let left = 0;
    let right = nums.length - 1;
    
    while (left < right) {
        const sum = nums[left] + nums[right];
        if (sum === target) {
            return [left, right];
        } else if (sum < target) {
            left++;
        } else {
            right--;
        }
    }
    return [];
}
```

### 2. Sliding Window
**Cuándo usar**: Subarrays, substrings, ventanas de tamaño fijo
**Complejidad**: O(n)
**Ejemplos**: Maximum Sum Subarray, Longest Substring Without Repeating Characters

```javascript
// Ejemplo: Maximum Sum Subarray of Size K
function maxSumSubarray(arr, k) {
    let maxSum = 0;
    let windowSum = 0;
    let start = 0;
    
    for (let end = 0; end < arr.length; end++) {
        windowSum += arr[end];
        
        if (end >= k - 1) {
            maxSum = Math.max(maxSum, windowSum);
            windowSum -= arr[start];
            start++;
        }
    }
    
    return maxSum;
}
```

### 3. Hash Map/Set
**Cuándo usar**: Búsquedas rápidas, conteos, duplicados
**Complejidad**: O(1) para operaciones básicas
**Ejemplos**: Two Sum, Group Anagrams, Longest Consecutive Sequence

```javascript
// Ejemplo: Group Anagrams
function groupAnagrams(strs) {
    const map = new Map();
    
    for (const str of strs) {
        const sorted = str.split('').sort().join('');
        if (!map.has(sorted)) {
            map.set(sorted, []);
        }
        map.get(sorted).push(str);
    }
    
    return Array.from(map.values());
}
```

### 4. Tree Traversal
**Cuándo usar**: Árboles binarios, búsquedas, recorridos
**Complejidad**: O(n)
**Ejemplos**: Binary Tree Inorder Traversal, Maximum Depth of Binary Tree

```javascript
// Ejemplo: Inorder Traversal (Recursive)
function inorderTraversal(root) {
    const result = [];
    
    function traverse(node) {
        if (!node) return;
        traverse(node.left);
        result.push(node.val);
        traverse(node.right);
    }
    
    traverse(root);
    return result;
}
```

### 5. Dynamic Programming
**Cuándo usar**: Problemas de optimización, subproblemas superpuestos
**Complejidad**: O(n) a O(n²)
**Ejemplos**: Fibonacci, Climbing Stairs, House Robber

```javascript
// Ejemplo: Fibonacci con DP
function fibonacci(n) {
    if (n <= 1) return n;
    
    const dp = [0, 1];
    for (let i = 2; i <= n; i++) {
        dp[i] = dp[i-1] + dp[i-2];
    }
    
    return dp[n];
}
```

### 6. Binary Search
**Cuándo usar**: Arrays ordenados, búsquedas eficientes
**Complejidad**: O(log n)
**Ejemplos**: Search in Rotated Sorted Array, Find Peak Element

```javascript
// Ejemplo: Binary Search
function binarySearch(nums, target) {
    let left = 0;
    let right = nums.length - 1;
    
    while (left <= right) {
        const mid = Math.floor((left + right) / 2);
        
        if (nums[mid] === target) {
            return mid;
        } else if (nums[mid] < target) {
            left = mid + 1;
        } else {
            right = mid - 1;
        }
    }
    
    return -1;
}
```

## 🎯 Plan de Estudio de 12 Semanas

### Semanas 1-2: Fundamentos
- **Arrays y Strings**: 20 problemas
- **Two Pointers**: 15 problemas
- **Hash Maps**: 15 problemas
- **Total**: 50 problemas

### Semanas 3-4: Estructuras de Datos
- **Linked Lists**: 15 problemas
- **Stacks y Queues**: 15 problemas
- **Trees**: 20 problemas
- **Total**: 50 problemas

### Semanas 5-6: Algoritmos de Búsqueda
- **Binary Search**: 20 problemas
- **Sliding Window**: 15 problemas
- **Backtracking**: 15 problemas
- **Total**: 50 problemas

### Semanas 7-8: Algoritmos Avanzados
- **Dynamic Programming**: 25 problemas
- **Greedy**: 15 problemas
- **Graphs**: 20 problemas
- **Total**: 60 problemas

### Semanas 9-10: Patrones Específicos
- **Trie**: 10 problemas
- **Union Find**: 10 problemas
- **Segment Tree**: 10 problemas
- **Total**: 30 problemas

### Semanas 11-12: Práctica Intensiva
- **Mock Interviews**: 20 entrevistas
- **Contests**: 5 competencias
- **Review**: Repaso de conceptos clave
- **Total**: 25+ problemas

## 🛠️ Herramientas Recomendadas

### Plataformas de Práctica
- **LeetCode**: 2000+ problemas, simulacros de entrevistas
- **HackerRank**: Problemas por categoría, certificaciones
- **CodeSignal**: Evaluaciones técnicas, challenges
- **InterviewBit**: Curso estructurado, problemas por dificultad

### IDEs y Editores
- **VS Code**: Con extensiones de LeetCode
- **IntelliJ IDEA**: Para Java
- **PyCharm**: Para Python
- **Online**: LeetCode, HackerRank, CodePen

### Recursos de Aprendizaje
- **Cracking the Coding Interview**: Libro clásico
- **Algorithms by Robert Sedgewick**: Teoría profunda
- **Grokking the Coding Interview**: Patrones algorítmicos
- **YouTube**: Canales como NeetCode, Back To Back SWE

## 📊 Métricas de Progreso

### Semanal
- **Problemas resueltos**: 15-20 por semana
- **Tiempo promedio**: < 30 minutos por problema
- **Accuracy**: > 80% en primera submissión
- **Mock interviews**: 2-3 por semana

### Mensual
- **Problemas totales**: 60-80 por mes
- **Patrones dominados**: 3-4 nuevos patrones
- **Complejidad**: Problemas de dificultad Hard
- **Contests**: Participación en 4+ competencias

## 🎯 Estrategias por Dificultad

### Easy (0-2 años experiencia)
- **Enfoque**: Comprensión de conceptos básicos
- **Tiempo**: 15-20 minutos por problema
- **Patrones**: Arrays, Strings, Hash Maps
- **Objetivo**: 100+ problemas Easy

### Medium (2-5 años experiencia)
- **Enfoque**: Aplicación de patrones algorítmicos
- **Tiempo**: 25-35 minutos por problema
- **Patrones**: Two Pointers, Sliding Window, DP
- **Objetivo**: 200+ problemas Medium

### Hard (5+ años experiencia)
- **Enfoque**: Optimización y casos edge
- **Tiempo**: 40-60 minutos por problema
- **Patrones**: Advanced DP, Graph Algorithms
- **Objetivo**: 50+ problemas Hard

## 🚨 Errores Comunes que Evitar

### ❌ En la Resolución
- No clarificar el problema completamente
- Saltarse los ejemplos
- No considerar casos edge
- Código desordenado sin comentarios
- No analizar complejidad

### ❌ En la Comunicación
- No explicar el enfoque antes de codificar
- No pensar en voz alta
- No pedir ayuda cuando se está atascado
- No probar la solución con ejemplos
- No discutir optimizaciones

### ❌ En la Práctica
- Solo hacer problemas fáciles
- No revisar soluciones después
- No practicar explicar el código
- No hacer mock interviews
- No repasar conceptos teóricos

## 🏆 Estrategias para Mock Interviews

### Preparación
- **Problema**: Leer y entender completamente
- **Ejemplos**: Crear 2-3 ejemplos propios
- **Enfoque**: Pensar en la estrategia general
- **Código**: Tener una idea de la implementación

### Durante la Entrevista
- **Comunicar**: Explicar cada paso del proceso
- **Preguntar**: Clarificar dudas sobre el problema
- **Ejemplos**: Usar ejemplos para validar la lógica
- **Optimizar**: Discutir mejoras y alternativas

### Después de la Entrevista
- **Review**: Revisar la solución y el código
- **Feedback**: Pedir feedback específico
- **Mejoras**: Identificar áreas de mejora
- **Práctica**: Trabajar en las debilidades identificadas

## 📈 Tracking de Progreso

### Hoja de Cálculo de Progreso
```markdown
| Fecha | Problema | Dificultad | Tiempo | Patrón | Notas |
|-------|----------|------------|--------|--------|-------|
| 2025-01-15 | Two Sum | Easy | 15min | Hash Map | Primera vez |
| 2025-01-15 | Valid Parentheses | Easy | 20min | Stack | Casos edge |
| 2025-01-16 | Maximum Subarray | Medium | 30min | DP | Kadane's algo |
```

### Métricas Importantes
- **Problemas por día**: 2-3 problemas
- **Tiempo promedio**: < 30 minutos
- **Accuracy rate**: > 80%
- **Patrones dominados**: 10+ patrones
- **Mock interviews**: 2-3 por semana

## 🎯 Problemas Esenciales por Categoría

### Arrays (20 problemas)
1. Two Sum
2. Best Time to Buy and Sell Stock
3. Contains Duplicate
4. Product of Array Except Self
5. Maximum Subarray
6. 3Sum
7. Container With Most Water
8. Rotate Array
9. Merge Intervals
10. Spiral Matrix

### Strings (15 problemas)
1. Valid Anagram
2. Valid Parentheses
3. Longest Substring Without Repeating Characters
4. Group Anagrams
5. Longest Palindromic Substring
6. Valid Palindrome
7. String to Integer
8. Longest Common Prefix
9. Find All Anagrams in a String
10. Minimum Window Substring

### Trees (20 problemas)
1. Maximum Depth of Binary Tree
2. Same Tree
3. Invert Binary Tree
4. Binary Tree Level Order Traversal
5. Validate Binary Search Tree
6. Path Sum
7. Binary Tree Maximum Path Sum
8. Lowest Common Ancestor
9. Serialize and Deserialize Binary Tree
10. Binary Tree Zigzag Level Order Traversal

### Dynamic Programming (25 problemas)
1. Climbing Stairs
2. House Robber
3. Longest Increasing Subsequence
4. Coin Change
5. Edit Distance
6. Longest Common Subsequence
7. Word Break
8. Unique Paths
9. Minimum Path Sum
10. Maximum Product Subarray

## 📚 Recursos Adicionales

### Libros Recomendados
- "Cracking the Coding Interview" - Gayle Laakmann McDowell
- "Algorithms" - Robert Sedgewick
- "Introduction to Algorithms" - Cormen, Leiserson, Rivest, Stein
- "Grokking the Coding Interview" - Design Gurus

### Cursos Online
- [LeetCode Explore](https://leetcode.com/explore/) - Curso estructurado
- [Algorithms Specialization](https://www.coursera.org/specializations/algorithms) - Coursera
- [CS50](https://cs50.harvard.edu/) - Harvard
- [MIT 6.006](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-006-introduction-to-algorithms-fall-2011/) - MIT

### Comunidades
- [r/leetcode](https://www.reddit.com/r/leetcode/) - Reddit
- [LeetCode Discuss](https://leetcode.com/discuss/) - Foros oficiales
- [Discord LeetCode](https://discord.gg/leetcode) - Comunidad Discord
- [Blind 75](https://www.teamblind.com/post/New-Year-Gift---Curated-List-of-Top-75-LeetCode-Questions-to-Save-Your-Time-OaM1OREU) - Lista curada

---

**¿Listo para dominar los algoritmos?** 🚀

[Siguiente: Portfolio Profesional →](./portfolio-profesional.md)

---

<div align="center">
  <p>💡 <strong>Tip:</strong> La consistencia es clave. Mejor 2 problemas por día durante 6 meses que 20 problemas en un fin de semana.</p>
</div>
