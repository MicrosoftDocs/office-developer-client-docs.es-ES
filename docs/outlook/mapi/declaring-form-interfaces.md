---
title: Declarar interfaces de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8f4d8842efbba2f1f2b7281e5d4741b89f975b3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816634"
---
# <a name="declaring-form-interfaces"></a>Declarar interfaces de formulario

  
  
**Hace referencia a**: Outlook 
  
Las declaraciones de las implementaciones de interfaces de formulario MAPI se pueden simplificar mediante el uso de las macros de _interface__METHOD MAPI_, donde _interfaz_ es una interfaz de formulario definida en el archivo de encabezado Mapiform.h. No es necesario usar estas macros, pero si no lo hace, debe tener especial cuidado que las declaraciones de cumplir con las declaraciones en el archivo de encabezado Mapiform.h. Por ejemplo, podría declarar la clase de objeto de formulario de su servidor de forma similar al siguiente: 
  
```cpp
class CMyForm : public IPersistMessage, public IMAPIForm,
                public IMAPIFormAdviseSink
{
public:
    CMyForm(CClassFactory *);    // constructorr takes a class factory object
    ~CMyForm(void);
// MAPI methods that need to be implemented.
    MAPI_IUNKNOWN_METHODS(IMPL);
    MAPI_GETLASTERROR_METHOD(IMPL);
    MAPI_IPERSISTMESSAGE_METHODS(IMPL);
    MAPI_IMAPIFORM_METHODS(IMPL);
    MAPI_IMAPIFORMADVISESINK_METHODS(IMPL);
// Add other implementation specific items.
};

```

## <a name="see-also"></a>Vea también



[Escribir código de servidor de formulario](writing-form-server-code.md)

