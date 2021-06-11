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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432957"
---
# <a name="implementing-objects-in-c"></a>Implementar objetos en C++

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes y proveedores de servicios de C++ definen objetos MAPI mediante la creación de clases que heredan de las interfaces que están implementando. Cada uno de los métodos de interfaz es público, al igual que el constructor y el destructor de la clase. Si la clase tiene métodos adicionales, pueden ser públicos o privados, según la implementación. Todos los miembros de datos son privados. 
  
En el siguiente código de ejemplo se muestra cómo definir un objeto de estado de C++. La `CMyMAPIObject` clase hereda de la [interfaz IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) Muchas de las macros usadas en este ejemplo se definen en el archivo de encabezado OLE Compobj.h. Los primeros miembros de la clase son los métodos de la interfaz base, seguidos de los métodos de las interfaces heredadas en orden de herencia. Después de las definiciones de interfaz se encuentran los métodos adicionales, el constructor y el destructor, y los miembros de datos. 
  
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

Para usar una instancia de la clase, los clientes o proveedores de servicios de C++ hacen una llamada a uno de  `CMyMAPIObject` sus métodos de la siguiente manera: 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>Vea también

- [Implementación de objetos MAPI](implementing-mapi-objects.md)

