---
title: Implementar objetos en C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 89247ca1b263d6f06af73f1ffa14709a2aff23de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310153"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="53a26-103">Implementar objetos en C++</span><span class="sxs-lookup"><span data-stu-id="53a26-103">Implementing objects in C++</span></span>

<span data-ttu-id="53a26-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53a26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53a26-105">Los clientes y proveedores de servicios de C++ definen los objetos MAPI mediante la creación de clases que heredan de las interfaces que están implementando.</span><span class="sxs-lookup"><span data-stu-id="53a26-105">C++ clients and service providers define MAPI objects by creating classes that inherit from the interfaces they are implementing.</span></span> <span data-ttu-id="53a26-106">Cada uno de los métodos de la interfaz es público, al igual que el constructor y el destructor de la clase.</span><span class="sxs-lookup"><span data-stu-id="53a26-106">Each of the interface methods is public, as are the constructor and destructor for the class.</span></span> <span data-ttu-id="53a26-107">Si la clase tiene métodos adicionales, pueden ser públicos o privados, en función de la implementación.</span><span class="sxs-lookup"><span data-stu-id="53a26-107">If the class has additional methods, they can be public or private, depending on the implementation.</span></span> <span data-ttu-id="53a26-108">Todos los miembros de datos son privados.</span><span class="sxs-lookup"><span data-stu-id="53a26-108">All data members are private.</span></span> 
  
<span data-ttu-id="53a26-109">En el código de ejemplo siguiente se muestra cómo definir un objeto de estado de C++.</span><span class="sxs-lookup"><span data-stu-id="53a26-109">The following example code shows how to define a C++ status object.</span></span> <span data-ttu-id="53a26-110">La `CMyMAPIObject` clase hereda de la interfaz [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="53a26-110">The  `CMyMAPIObject` class inherits from the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="53a26-111">Muchas de las macros usadas en este ejemplo se definen en el archivo de encabezado OLE COMPOBJ. h.</span><span class="sxs-lookup"><span data-stu-id="53a26-111">Many of the macros used in this example are defined in the OLE header file Compobj.h.</span></span> <span data-ttu-id="53a26-112">Los primeros miembros de la clase son los métodos de la interfaz base, seguidos de los métodos de las interfaces heredadas en orden de herencia.</span><span class="sxs-lookup"><span data-stu-id="53a26-112">The first members of the class are the methods of the base interface, followed by the methods of the inherited interfaces in order of inheritance.</span></span> <span data-ttu-id="53a26-113">El seguimiento de las definiciones de interfaz son métodos adicionales, el constructor y el destructor y los miembros de datos.</span><span class="sxs-lookup"><span data-stu-id="53a26-113">Following the interface definitions are any additional methods, the constructor and destructor, and the data members.</span></span> 
  
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

<span data-ttu-id="53a26-114">Para usar una instancia de la `CMyMAPIObject` clase, los clientes o proveedores de servicios de C++ realizan una llamada a uno de sus métodos de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="53a26-114">To use an instance of the  `CMyMAPIObject` class, C++ clients or service providers make a call to one of its methods as follows:</span></span> 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a><span data-ttu-id="53a26-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="53a26-115">See also</span></span>

- [<span data-ttu-id="53a26-116">Implementación de objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="53a26-116">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

