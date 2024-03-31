<br> https://pujithavege.github.io/HomePage/<br>

Login page using react:
npx create-react-app login-form-app
cd login-form-app
-----------
LoginForm.js:
// src/LoginForm.js
import React, { useState } from 'react';

const LoginForm = ({ onSubmit }) => {
  const [username, setUsername] = useState('');
  const [password, setPassword] = useState('');

  const handleSubmit = (e) => {
    e.preventDefault();
    onSubmit({ username, password });
  };

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="text"
        placeholder="Username"
        value={username}
        onChange={(e) => setUsername(e.target.value)}
      />
      <input
        type="password"
        placeholder="Password"
        value={password}
        onChange={(e) => setPassword(e.target.value)}
      />
      <button type="submit">Login</button>
    </form>
  );
};

export default LoginForm;
-----------------
Logo.js:
// src/Logo.js
import React from 'react';

const Logo = () => {
  return (
    <div>
      <h1>Company Logo</h1>
      {/* Add your logo here */}
    </div>
  );
};

export default Logo;

----------------
ComapanyName.js:
// src/CompanyName.js
import React from 'react';

const CompanyName = () => {
  return <h2>Company Name</h2>;
};

export default CompanyName;
--------------------
App.js:
// src/App.js
import React from 'react';
import './App.css';
import Logo from './Logo';
import CompanyName from './CompanyName';
import LoginForm from './LoginForm';

const App = () => {
  const handleSubmit = (credentials) => {
    // Handle login logic here
    console.log('Submitted:', credentials);
  };

  return (
    <div className="App">
      <div className="header">
        <Logo />
        <CompanyName />
      </div>
      <div className="login-form">
        <LoginForm onSubmit={handleSubmit} />
      </div>
    </div>
  );
};

export default App;
-----------------------
App.css:
/* src/App.css */
.App {
  text-align: center;
}

.header {
  margin-bottom: 20px;
}

.login-form {
  width: 300px;
  margin: 0 auto;
}

input {
  margin-bottom: 10px;
}
----------------------------------------
React2 Registration form:
UserDetails.js:
import React, { useState } from 'react';

const UserDetails = ({ onChange }) => {
  const [firstName, setFirstName] = useState('');
  const [lastName, setLastName] = useState('');
  const [dob, setDob] = useState('');

  const handleInputChange = (e) => {
    const { name, value } = e.target;
    onChange({ [name]: value });
  };

  return (
    <div>
      <h2>User Details</h2>
      <input
        type="text"
        name="firstName"
        placeholder="First Name"
        value={firstName}
        onChange={(e) => setFirstName(e.target.value)}
        onBlur={handleInputChange}
      />
      <input
        type="text"
        name="lastName"
        placeholder="Last Name"
        value={lastName}
        onChange={(e) => setLastName(e.target.value)}
        onBlur={handleInputChange}
      />
      <input
        type="date"
        name="dob"
        placeholder="Date of Birth"
        value={dob}
        onChange={(e) => setDob(e.target.value)}
        onBlur={handleInputChange}
      />
    </div>
  );
};

export default UserDetails;
-------------------------
ContactInfo.js:
import React, { useState } from 'react';

const ContactInfo = ({ onChange }) => {
  const [email, setEmail] = useState('');
  const [phone, setPhone] = useState('');
  const [linkedin, setLinkedin] = useState('');

  const handleInputChange = (e) => {
    const { name, value } = e.target;
    onChange({ [name]: value });
  };

  return (
    <div>
      <h2>Contact Info</h2>
      <input
        type="email"
        name="email"
        placeholder="Email"
        value={email}
        onChange={(e) => setEmail(e.target.value)}
        onBlur={handleInputChange}
      />
      <input
        type="tel"
        name="phone"
        placeholder="Phone"
        value={phone}
        onChange={(e) => setPhone(e.target.value)}
        onBlur={handleInputChange}
      />
      <input
        type="text"
        name="linkedin"
        placeholder="LinkedIn"
        value={linkedin}
        onChange={(e) => setLinkedin(e.target.value)}
        onBlur={handleInputChange}
      />
    </div>
  );
};

export default ContactInfo;
-----------------------
Address.js:
import React, { useState } from 'react';

const Address = ({ onChange }) => {
  const [doorNo, setDoorNo] = useState('');
  const [flatNo, setFlatNo] = useState('');
  const [street1, setStreet1] = useState('');
  const [street2, setStreet2] = useState('');
  const [city, setCity] = useState('');
  const [state, setState] = useState('');
  const [country, setCountry] = useState('');
  const [pinCode, setPinCode] = useState('');

  const handleInputChange = (e) => {
    const { name, value } = e.target;
    onChange({ [name]: value });
  };

  return (
    <div>
      <h2>Address</h2>
      <input
        type="text"
        name="doorNo"
        placeholder="Door No"
        value={doorNo}
        onChange={(e) => setDoorNo(e.target.value)}
        onBlur={handleInputChange}
      />
      <input
        type="text"
        name="flatNo"
        placeholder="Flat No"
        value={flatNo}
        onChange={(e) => setFlatNo(e.target.value)}
        onBlur={handleInputChange}
      />
      <input
        type="text"
        name="street1"
        placeholder="Street Name 1"
        value={street1}
        onChange={(e) => setStreet1(e.target.value)}
        onBlur={handleInputChange}
      />
      <input
        type="text"
        name="street2"
        placeholder="Street Name 2"
        value={street2}
        onChange={(e) => setStreet2(e.target.value)}
        onBlur={handleInputChange}
      />
      <input
        type="text"
        name="city"
        placeholder="City"
        value={city}
        onChange={(e) => setCity(e.target.value)}
        onBlur={handleInputChange}
      />
      <input
        type="text"
        name="state"
        placeholder="State"
        value={state}
        onChange={(e) => setState(e.target.value)}
        onBlur={handleInputChange}
      />
      <input
        type="text"
        name="country"
        placeholder="Country"
        value={country}
        onChange={(e) => setCountry(e.target.value)}
        onBlur={handleInputChange}
      />
      <input
        type="text"
        name="pinCode"
        placeholder="PIN Code"
        value={pinCode}
        onChange={(e) => setPinCode(e.target.value)}
        onBlur={handleInputChange}
      />
    </div>
  );
};

export default Address;
------------------
SubmitResetButtons.js:
import React from 'react';

const SubmitResetButtons = ({ onSubmit, onReset }) => {
  return (
    <div>
      <button onClick={onSubmit}>Submit</button>
      <button onClick={onReset}>Reset</button>
    </div>
  );
};

export default SubmitResetButtons;
------------------
App.js:
import React, { useState } from 'react';
import UserDetails from './UserDetails';
import ContactInfo from './ContactInfo';
import Address from './Address';
import SubmitResetButtons from './SubmitResetButtons';

function App() {
  const [userData, setUserData] = useState({
    userDetails: {},
    contactInfo: {},
    address: {},
  });

  const handleSubmit = () => {
    // Handle form submission
    console.log('Submitted:', userData);
  };

  const handleReset = () => {
    // Reset form fields
    setUserData({
      userDetails: {},
      contactInfo: {},
      address: {},
    });
  };

  const handleUserDataChange = (data) => {
    setUserData((prevData) => ({
      ...prevData,
      userDetails: { ...prevData.userDetails, ...data },
    }));
  };

  const handleContactInfoChange = (data) => {
    setUserData((prevData) => ({
      ...prevData,
      contactInfo: { ...prevData.contactInfo, ...data },
    }));
  };

  const handleAddressChange = (data) => {
    setUserData((prevData) => ({
      ...prevData,
      address: { ...prevData.address, ...data },
    }));
  };

  return (
    <div>
      <h1>User Registration Form</h1>
      <UserDetails onChange={handleUserDataChange} />
      <ContactInfo onChange={handleContactInfoChange} />
      <Address onChange={handleAddressChange} />
      <SubmitResetButtons onSubmit={handleSubmit} onReset={handleReset} />
    </div>
  );
}

export default App;


