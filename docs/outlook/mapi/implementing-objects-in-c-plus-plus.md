---
title: Implementación de objetos de C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: ea9f37183f33459b09f2730b3efbb7afed3d4766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817691"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="a6700-103">Implementación de objetos de C++</span><span class="sxs-lookup"><span data-stu-id="a6700-103">Implementing objects in C++</span></span>

<span data-ttu-id="a6700-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6700-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6700-105">Proveedores de servicios y los clientes de C++ definición objetos MAPI mediante la creación de clases que heredan de las interfaces que están implementando.</span><span class="sxs-lookup"><span data-stu-id="a6700-105">C++ clients and service providers define MAPI objects by creating classes that inherit from the interfaces they are implementing.</span></span> <span data-ttu-id="a6700-106">Cada uno de los métodos de interfaz es pública, como son el constructor y el destructor para la clase.</span><span class="sxs-lookup"><span data-stu-id="a6700-106">Each of the interface methods is public, as are the constructor and destructor for the class.</span></span> <span data-ttu-id="a6700-107">Si la clase tiene métodos adicionales, pueden ser públicas o privadas, dependiendo de la implementación.</span><span class="sxs-lookup"><span data-stu-id="a6700-107">If the class has additional methods, they can be public or private, depending on the implementation.</span></span> <span data-ttu-id="a6700-108">Todos los miembros de datos son privados.</span><span class="sxs-lookup"><span data-stu-id="a6700-108">All data members are private.</span></span> 
  
<span data-ttu-id="a6700-109">El ejemplo de código siguiente muestra cómo definir un objeto de estado de C++.</span><span class="sxs-lookup"><span data-stu-id="a6700-109">The following example code shows how to define a C++ status object.</span></span> <span data-ttu-id="a6700-110">El `CMyMAPIObject` clase hereda de la [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="a6700-110">The  `CMyMAPIObject` class inherits from the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="a6700-111">Muchas de las macros que se usa en este ejemplo se definen en el archivo de encabezado OLE Compobj.h.</span><span class="sxs-lookup"><span data-stu-id="a6700-111">Many of the macros used in this example are defined in the OLE header file Compobj.h.</span></span> <span data-ttu-id="a6700-112">El primer los miembros de la clase son los métodos de la interfaz base, seguido de los métodos de las interfaces heredadas en orden de herencia.</span><span class="sxs-lookup"><span data-stu-id="a6700-112">The first members of the class are the methods of the base interface, followed by the methods of the inherited interfaces in order of inheritance.</span></span> <span data-ttu-id="a6700-113">Siguiendo las definiciones de interfaz es métodos adicionales, el constructor y destructor y los miembros de datos.</span><span class="sxs-lookup"><span data-stu-id="a6700-113">Following the interface definitions are any additional methods, the constructor and destructor, and the data members.</span></span> 
  
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

<span data-ttu-id="a6700-114">Para usar una instancia de la `CMyMAPIObject` clase, los clientes de C++ o proveedores de servicios de realizar una llamada a uno de sus métodos de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="a6700-114">To use an instance of the  `CMyMAPIObject` class, C++ clients or service providers make a call to one of its methods as follows:</span></span> 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a><span data-ttu-id="a6700-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="a6700-115">See also</span></span>

- [<span data-ttu-id="a6700-116">Implementación de objetos de MAPI</span><span class="sxs-lookup"><span data-stu-id="a6700-116">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

