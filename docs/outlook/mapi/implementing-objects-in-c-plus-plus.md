---
title: Implementación de objetos de C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4c233f9855674080496b2e54ba9548a53738ead8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574730"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="bc92b-103">Implementación de objetos de C++</span><span class="sxs-lookup"><span data-stu-id="bc92b-103">Implementing objects in C++</span></span>

<span data-ttu-id="bc92b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc92b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc92b-105">Proveedores de servicios y los clientes de C++ definición objetos MAPI mediante la creación de clases que heredan de las interfaces que están implementando.</span><span class="sxs-lookup"><span data-stu-id="bc92b-105">C++ clients and service providers define MAPI objects by creating classes that inherit from the interfaces they are implementing.</span></span> <span data-ttu-id="bc92b-106">Cada uno de los métodos de interfaz es pública, como son el constructor y el destructor para la clase.</span><span class="sxs-lookup"><span data-stu-id="bc92b-106">Each of the interface methods is public, as are the constructor and destructor for the class.</span></span> <span data-ttu-id="bc92b-107">Si la clase tiene métodos adicionales, pueden ser públicas o privadas, dependiendo de la implementación.</span><span class="sxs-lookup"><span data-stu-id="bc92b-107">If the class has additional methods, they can be public or private, depending on the implementation.</span></span> <span data-ttu-id="bc92b-108">Todos los miembros de datos son privados.</span><span class="sxs-lookup"><span data-stu-id="bc92b-108">All data members are private.</span></span> 
  
<span data-ttu-id="bc92b-109">El ejemplo de código siguiente muestra cómo definir un objeto de estado de C++.</span><span class="sxs-lookup"><span data-stu-id="bc92b-109">The following example code shows how to define a C++ status object.</span></span> <span data-ttu-id="bc92b-110">El `CMyMAPIObject` clase hereda de la [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="bc92b-110">The  `CMyMAPIObject` class inherits from the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="bc92b-111">Muchas de las macros que se usa en este ejemplo se definen en el archivo de encabezado OLE Compobj.h.</span><span class="sxs-lookup"><span data-stu-id="bc92b-111">Many of the macros used in this example are defined in the OLE header file Compobj.h.</span></span> <span data-ttu-id="bc92b-112">El primer los miembros de la clase son los métodos de la interfaz base, seguido de los métodos de las interfaces heredadas en orden de herencia.</span><span class="sxs-lookup"><span data-stu-id="bc92b-112">The first members of the class are the methods of the base interface, followed by the methods of the inherited interfaces in order of inheritance.</span></span> <span data-ttu-id="bc92b-113">Siguiendo las definiciones de interfaz es métodos adicionales, el constructor y destructor y los miembros de datos.</span><span class="sxs-lookup"><span data-stu-id="bc92b-113">Following the interface definitions are any additional methods, the constructor and destructor, and the data members.</span></span> 
  
```cpp
class  CMyMAPIObject : public IMAPIStatus
{
public:
// Methods of IUnknown.
    STDMETHODIMP QueryInterface (REFIID riid, LPVOID * ppvObj);
    STDMETHODIMP_(ULONG) AddRef ();
    STDMETHODIMP_(ULONG) Release ();
    MAPI_IMAPIPROP_METHODS(IMPL);
    MAPI_IMAPISTATUS_METHODS(IMPL);
// Other methods specific to CMyMAPIObject.
    BOOL WINAPI Method1 ();
    void WINAPI Method2 ();
// Constructors and destructors.
public :
    CMyMAPIObject () {};
    ~CMyMAPIObject () {};
// Data members specific to CMyMAPIObject.
private :
    ULONG               m_cRef;
    CAnotherObj *       m_pObj;
};
 
```

<span data-ttu-id="bc92b-114">Para usar una instancia de la `CMyMAPIObject` clase, los clientes de C++ o proveedores de servicios de realizar una llamada a uno de sus métodos de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="bc92b-114">To use an instance of the  `CMyMAPIObject` class, C++ clients or service providers make a call to one of its methods as follows:</span></span> 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a><span data-ttu-id="bc92b-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="bc92b-115">See also</span></span>

- [<span data-ttu-id="bc92b-116">Implementar objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="bc92b-116">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

