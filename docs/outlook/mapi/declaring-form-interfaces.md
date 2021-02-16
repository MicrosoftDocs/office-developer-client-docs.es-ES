---
title: Declaración de interfaces de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0fa742b7ff6d98e3a0f475accbc440d22eac0919
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437514"
---
# <a name="declaring-form-interfaces"></a>Declaración de interfaces de formulario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Puede simplificar las declaraciones de las implementaciones de interfaces de formulario MAPI mediante las macros de MAPI_ _interface__METHOD, donde  _la_ interfaz es una interfaz de formulario definida en el archivo de encabezado Mapiform.h. No es necesario que use estas macros, pero si no lo hace, debe tener especial cuidado de que las declaraciones se ajustan a las declaraciones en el archivo de encabezado Mapiform.h. Por ejemplo, puede declarar la clase de objeto de formulario del servidor de formulario de la siguiente manera: 
  
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

## <a name="see-also"></a>Consulte también



[Escritura de código de servidor de formulario](writing-form-server-code.md)

