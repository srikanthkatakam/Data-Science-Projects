# Prediction of Patient no-show in a clinic/hospital

Hospital appointment where the patient does not turn-up is defined as an appointment in which the patient did not visit for the treatment or cancelled the same day. As these appointments are problematic for practices at all levels of the health care system, patients not turning up is a missed revenue opportunity which cannot be re-captured for the practice, and which contribute to both decreased patient and staff satisfaction. Such appointments negatively impact both patients and care teams. The objective is to predict the probability of a patient not turning up for a medical appointment.

### Data

This analysis consists of exploring a dataset containing approximately 100k medical appointments from the Brazilian public health system known as SUS (Single Health System).

### Attributes Description

- `PatientId:` Identification of a patient

- `AppointmentID:` Identification of each appointment

- `Gender:` Male or Female

- `ScheduledDay:` The day someone called or registered the appointment

- `AppointmentDay:` The day of the actual appointment, when they have to visit the doctor

- `Age:` How old is the patient

- `Neighbourhood:` Where the appointment takes place

- `Scholarship:` True or False, indicates if the patient is in the Bolsa Familia program (a social welfare program of the Government of Brazil)

- `Hypertension:` True or False

- `Diabetes:` True or False

- `Alcoholism:` True or False

- `Handicap:` True or False

- `SMS_received:` 1 or more messages sent to the patient

- `No-show:` "No" indicates if the patient attended to their appointment and "Yes" if they didn't attend

### Evaluation Metric: Recall

For this problem, minimizing Type II errors is a priority. A Type II error here is a situation where the algorithm incorrectly posits a patient will turn up for an appointment, but they do not present themselves for the scheduled appointment. The inverse situation, in which the prediction is a patient no-attendance, but they do attend the appointment is less of a burden on the practice and has fewer negative impacts for the patient than not receiving care. The prediction as no-attendance, but the patient does attend, is the Type I error. The most successful algorithm is defined as one with high recall.
