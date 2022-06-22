# PHPDependentDropdown

CREATE TABLE `country` (
  `id` int(11) NOT NULL PRIMARY KEY AUTO_INCREMENT,
  `name` varchar(255) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `country`
--

INSERT INTO `country` (`id`, `name`) VALUES
(1, 'india'),
(2, 'pakistan'),
(3, 'nepal'),
(4, 'usa');

-- --------------------------------------------------------

--
-- Table structure for table `state`
--

CREATE TABLE `state` (
  `id` int(11) NOT NULL PRIMARY KEY AUTO_INCREMENT,
  `country_id` int(11) NOT NULL,
  `state` varchar(255) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `state`
--

INSERT INTO `state` (`id`, `country_id`, `state`) VALUES
(1, 1, 'bihar'),
(2, 1, 'delhi'),
(3, 2, 'sindh'),
(4, 2, 'islamabad'),
(5, 3, 'Rapti'),
(6, 3, 'Kamali'),
(7, 4, 'new york'),
(8, 4, 'california');


--
-- Table structure for table `city`
--

CREATE TABLE `city` (
  `id` int(11) NOT NULL PRIMARY KEY AUTO_INCREMENT,
  `state_id` int(11) NOT NULL,
  `city` varchar(255) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;


--
-- Dumping data for table `city`
--

INSERT INTO `city` (`id`, `state_id`, `city`) VALUES
(1, 1, 'patna'),
(2, 1, 'siwan'),
(3, 2, 'chandani chowk'),
(4, 2, 'rajiv chowk'),
(5, 3, 'karachi'),
(6, 4, 'khaipur'),
(7, 5, 'kathmandu'),
(8, 6, 'nepla city'),
(9, 7, 'new york city 1'),
(10, 7, 'new york city 2\r\n'),
(11, 8, 'california city 1'),
(12, 8, 'california city 2');
