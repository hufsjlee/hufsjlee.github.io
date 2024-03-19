---
title: "이분탐색(Binary Search)"
excerpt: "이분탐색(Binary Search)이란?"

categories:
  - OS
tags:
  - [tag1, tag2]

permalink: /os/binarysearch/

toc: true
toc_sticky: true

date: 2024-03-19
last_modified_at: 2024-03-19
---

## 🔎 본문

## 이분탐색 (Binary Search)

### 이분탐색이란?
이분 탐색은 오름차순 또는 내림차순으로 **정렬된** 수열에서 검색하는 알고리즘이다. 선형 탐색보다 훨씬 빠르게 탐색할 수 있다는 장점이 있다. 시간복잡도는 탐색할 범위를 절반으로 줄여서 탐색하므로 **O(logn)**이다.

이분 탐색은 아래와 같은 과정으로 이루어진다.

1. 배열의 가운데 요소의 인덱스를 pivot으로 정한다.
2. a[pivot]의 값이 찾고자 하는 요소와 같다면 검색완료
3. a[pivot]의 값이 찾는 값보다 크다면 left ~ pivot 사이를 탐색한다.
4. a[pivot]의 값이 찾는 값보다 작다면 pivot ~ right 사이를 탐색한다.

## 코드

```Java
import java.util.Scanner;

public class BinarySearch {
    public static void main(String[] args) {
        int[] a = { 2, 17, 19, 21, 45, 50, 55, 72, 80, 120 };
        Scanner scanner = new Scanner(System.in);
        int key = scanner.nextInt();

        int left = 0;
        int right = 9;
        boolean flag = false;
        while (left <= right) {
            System.out.println("left: " + left + ", right: " + right);
            int pivot = (left + right) / 2;
            if (a[pivot] == key) {
                flag = true;
                System.out.println(pivot);
                break;
            } else if (a[pivot] < key) {
                left = pivot + 1;
            } else {
                right = pivot - 1;
            }
        }

        if (!flag) {
            System.out.println("검색 실패");
        }
    }
}

```




