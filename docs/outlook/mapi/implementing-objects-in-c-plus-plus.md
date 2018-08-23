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
# <a name="implementing-objects-in-c"></a>Implementación de objetos de C++

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proveedores de servicios y los clientes de C++ definición objetos MAPI mediante la creación de clases que heredan de las interfaces que están implementando. Cada uno de los métodos de interfaz es pública, como son el constructor y el destructor para la clase. Si la clase tiene métodos adicionales, pueden ser públicas o privadas, dependiendo de la implementación. Todos los miembros de datos son privados. 
  
El ejemplo de código siguiente muestra cómo definir un objeto de estado de C++. El `CMyMAPIObject` clase hereda de la [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interfaz. Muchas de las macros que se usa en este ejemplo se definen en el archivo de encabezado OLE Compobj.h. El primer los miembros de la clase son los métodos de la interfaz base, seguido de los métodos de las interfaces heredadas en orden de herencia. Siguiendo las definiciones de interfaz es métodos adicionales, el constructor y destructor y los miembros de datos. 
  
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

Para usar una instancia de la `CMyMAPIObject` clase, los clientes de C++ o proveedores de servicios de realizar una llamada a uno de sus métodos de la siguiente manera: 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>Recursos adicionales

- [Implementar objetos MAPI](implementing-mapi-objects.md)

