# 퀴즈 데이터 JSON 작성 방법

```json
{
    "name": "Example Quiz Title", // 퀴즈 제목(이름)
    "description": "Example Quiz Description", // 퀴즈 설명
    "authors": ["Kim", "Lee"], // 퀴즈 작성자(배열로 작성)
    "lastUpdated": "2025-01-01", // 퀴즈 마지막 업데이트 날짜
    "questions": [ // 퀴즈 문제
        {
            "question": "What is OOO?", // 문제 내용
            "options": [ // 문제 선택지
                "Option 1",
                "Option 2",
                "Option 3",
                "Option 4"
            ],
            "correct": "Option 1", // 정답
            "explanation": "Explanation of the correct answer.", // 정답 설명
            "hint": "Hint for the question.", // 힌트 (옵션)
            "difficulty": "easy", // 난이도 (easy, normal, hard) (옵션)
        }
    ]
}
```

```ts
interface Quiz {
    name: string
    description: string
    questions: Array<Question>
}

interface Question {
    question: string
    options: Array<string>
    correct: string
    explanation: string
    hint?: string
    difficulty?: 'easy' | 'normal' | 'hard'
}
```
