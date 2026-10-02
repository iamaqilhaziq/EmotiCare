# Emotional Assessment

## Overview

This pseudocode represents the general assessment workflow used within EmotiCare.

EmotiCare supports multiple structured emotional and psychological assessment modules, including:

- DASS-21
- SSEIT

Users are required to select an answer for the current question before proceeding to the next question.

---

## Pseudocode

```text
BEGIN

    USER selects an assessment

    CHECK assessment availability

    IF assessment is available THEN

        LOAD assessment questions

        SET current question = first question

        WHILE current question exists

            DISPLAY current question

            WAIT for user to select an answer

            IF answer is selected THEN

                RECORD selected answer

                ENABLE progression to next question

                IF current question is not the final question THEN

                    USER proceeds to next question

                    LOAD next question

                ELSE

                    ENABLE assessment submission

                END IF

            ELSE

                PREVENT progression to next question

            END IF

        END WHILE

        USER submits completed assessment

        CALCULATE assessment score
        according to selected assessment

        DETERMINE result category

        STORE assessment result

        DISPLAY assessment result

        PROVIDE relevant result information

    ELSE

        PREVENT assessment from starting

    END IF

END
```

---

## Assessment Flow

```text
Select Assessment
       │
       ▼
Load First Question
       │
       ▼
Display Question
       │
       ▼
Select Answer
       │
       ▼
Is Answer Selected?
       │
       ├── No ──────► Cannot Proceed
       │                 │
       │                 └────► Remain on Current Question
       │
       └── Yes
              │
              ▼
        Record Answer
              │
              ▼
       Final Question?
              │
       ┌──────┴──────┐
       │             │
      No            Yes
       │             │
       ▼             ▼
 Next Question    Submit Assessment
                     │
                     ▼
               Calculate Score
                     │
                     ▼
              Determine Result
                     │
                     ▼
                Store Result
                     │
                     ▼
               Display Result
```

---

## Supported Assessments

The general workflow applies to the assessment modules available within EmotiCare:

| Assessment | Module |
|---|---|
| DASS-21 | Emotional assessment |
| SSEIT | Emotional intelligence assessment |

Each assessment follows its respective scoring and result interpretation method.

---

## Assessment Navigation Rule

For every assessment:

- One question is presented at a time.
- The user must select an answer for the current question.
- The user cannot proceed to the next question without selecting an answer.
- After an answer is selected, progression to the next question is allowed.
- The assessment can only be submitted after reaching and answering the final question.

---

> **Note:** This pseudocode represents the general assessment workflow and does not expose the production scoring algorithms, database queries, or implementation details.