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
ms.openlocfilehash: 0fa742b7ff6d98e3a0f475accbc440d22eac0919
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437514"
---
# <a name="declaring-form-interfaces"></a>Declarar interfaces de formulario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Puede simplificar las declaraciones de las implementaciones de las interfaces de formulario MAPI mediante el uso de las macros MAPI_ _interface__METHOD, donde _interfaz_ es una interfaz de formulario definida en el archivo de encabezado MAPIForm. h. No es necesario que use estas macros, pero si no es así, debe tener especial cuidado de que las declaraciones se ajusten a las declaraciones del archivo de encabezado MAPIForm. h. Por ejemplo, puede declarar la clase del objeto Form del servidor de formulario como se indica a continuación: 
  
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

## <a name="see-also"></a>Ver también



[Escribir código de servidor de formulario](writing-form-server-code.md)

