
A Zend\ServiceManager\ServiceManager is an implementation of Zend\ServiceManager\ServiceLocatorInterface. Its task is to provide
a service or retrieving other objects based on the service name.

*ServiceLocatorInterface*

namespace Zend\ServiceManager

public interface ServiceLocatorInterface
{
public function get ($name);
public function has($name);
}

In addition of implementing the above inteface, a Zend\ServiceManager\ServiceManager provides following addition API

*Service Registraion *
*Lazy-loaded Service Objects*
*Service Factories *
*Service Aliasing *
*Abstract Factories *
*Initializers *
