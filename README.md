# Prohealth
SOURCE CODE
CREATE TABLE `appointments`
(
  `id` int(11) NOT NULL,
  `patient_id` int(11) DEFAULT NULL,
  `doctor_id` int(11) DEFAULT NULL,
  `appointment_date` datetime DEFAULT NULL,
  `cause` varchar(5000) DEFAULT NULL
) 
INSERT INTO `appointments` (`id`, `patient_id`, `doctor_id`, `appointment_date`, `cause`) VALUES
(1, 1, 2, '2025-05-04 09:00:00', '0'),
(2, 1, 3, '2025-05-04 09:00:00', '0'),
(3, 1, 2, '2025-05-04 09:30:00', 'Cough - Chest pain'),
(4, 1, 2, '2025-05-04 10:00:00', 'Skipped'),
(5, 1, 2, '2025-05-08 09:00:00', 'Skipped');
CREATE TABLE BEDS
(
  `id` int(11) NOT NULL,
  `number` varchar(10) NOT NULL,
  `ward_id` int(11) NOT NULL,
  `status` enum('available','occupied') DEFAULT 'available',
  `patient_id` int(11) DEFAULT NULL
) 
CREATE TABLE `DOCTORS
(
  `id` int(11) NOT NULL,
  `firstname` varchar(50) DEFAULT NULL,
  ...
  `fees` varchar(255) DEFAULT NULL
) 
CREATE TABLE MANAGER 
(
  `id` int(11) NOT NULL,
  `firstname` varchar(50) DEFAULT NULL,
  ...
  `profile_pic` varchar(255) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

