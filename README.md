import React from 'react';
import { 
  User, 
  Mail, 
  Linkedin, 
  Kaggle, 
  PythonIcon, 
  JavaIcon, 
  TensorFlowIcon, 
  AWSIcon, 
  GitIcon 
} from 'lucide-react';

const ModernProfilePage = () => {
  const skills = [
    { name: 'Python', icon: PythonIcon, color: 'text-blue-600' },
    { name: 'Java', icon: JavaIcon, color: 'text-red-600' },
    { name: 'TensorFlow', icon: TensorFlowIcon, color: 'text-orange-600' },
    { name: 'AWS', icon: AWSIcon, color: 'text-yellow-500' },
    { name: 'Git', icon: GitIcon, color: 'text-red-500' }
  ];

  return (
    <div className="min-h-screen bg-gradient-to-br from-gray-100 to-gray-200 flex items-center justify-center p-4">
      <div className="bg-white shadow-2xl rounded-2xl max-w-4xl w-full p-8 grid md:grid-cols-3 gap-8">
        {/* Profile Image & Basic Info */}
        <div className="md:col-span-1 flex flex-col items-center">
          <img 
            src="/api/placeholder/300/300" 
            alt="Lakshan Cooray" 
            className="w-64 h-64 rounded-full object-cover border-4 border-blue-500 shadow-lg"
          />
          <h1 className="text-2xl font-bold mt-4 text-gray-800">Lakshan Cooray</h1>
          <p className="text-blue-600 font-medium">Data Science Student</p>
        </div>

        {/* About & Contact */}
        <div className="md:col-span-2 space-y-6">
          <div className="bg-blue-50 p-4 rounded-xl">
            <h2 className="text-xl font-semibold text-gray-800 mb-4 flex items-center">
              <User className="mr-2 text-blue-600" /> About Me
            </h2>
            <p className="text-gray-600">
              Passionate Data Science student specializing in Machine Learning and Deep Learning. 
              Continuously exploring the intersections of advanced algorithms and practical applications.
            </p>
          </div>

          {/* Contact & Social */}
          <div className="grid md:grid-cols-2 gap-4">
            <div className="bg-green-50 p-4 rounded-xl">
              <h3 className="text-lg font-semibold text-gray-800 mb-3 flex items-center">
                <Mail className="mr-2 text-green-600" /> Contact
              </h3>
              <p className="text-gray-700">lakshancooray23@gmail.com</p>
            </div>

            <div className="bg-indigo-50 p-4 rounded-xl">
              <h3 className="text-lg font-semibold text-gray-800 mb-3">Connect</h3>
              <div className="flex space-x-4">
                <a 
                  href="https://www.linkedin.com/in/lakshan-cooray/" 
                  target="_blank" 
                  className="hover:bg-blue-100 p-2 rounded-full transition"
                >
                  <Linkedin className="text-blue-600 w-6 h-6" />
                </a>
                <a 
                  href="https://www.kaggle.com/lakshancooray23" 
                  target="_blank" 
                  className="hover:bg-blue-100 p-2 rounded-full transition"
                >
                  <Kaggle className="text-blue-600 w-6 h-6" />
                </a>
              </div>
            </div>
          </div>

          {/* Skills */}
          <div className="bg-purple-50 p-4 rounded-xl">
            <h2 className="text-xl font-semibold text-gray-800 mb-4">Skills</h2>
            <div className="flex flex-wrap gap-3">
              {skills.map((skill) => (
                <div 
                  key={skill.name} 
                  className="flex items-center bg-white shadow-md rounded-full px-3 py-1"
                >
                  <skill.icon className={`mr-2 ${skill.color} w-5 h-5`} />
                  <span className="text-gray-700">{skill.name}</span>
                </div>
              ))}
            </div>
          </div>
        </div>
      </div>
    </div>
  );
};

export default ModernProfilePage;
