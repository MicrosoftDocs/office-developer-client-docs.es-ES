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
# <a name="declaring-form-interfaces"></a><span data-ttu-id="ff6e1-103">Declaración de interfaces de formulario</span><span class="sxs-lookup"><span data-stu-id="ff6e1-103">Declaring Form Interfaces</span></span>

  
  
<span data-ttu-id="ff6e1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff6e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff6e1-105">Puede simplificar las declaraciones de las implementaciones de interfaces de formulario MAPI mediante las macros de MAPI_ _interface__METHOD, donde  _interface_ es una interfaz de formulario definida en el archivo de encabezado Mapiform.h.</span><span class="sxs-lookup"><span data-stu-id="ff6e1-105">You can simplify the declarations of your implementations of MAPI form interfaces by using the MAPI_ _interface__METHOD macros, where  _interface_ is a form interface defined in the Mapiform.h header file.</span></span> <span data-ttu-id="ff6e1-106">No es necesario que use estas macros, pero si no lo hace, debe tener especial cuidado de que las declaraciones se ajusten a las declaraciones del archivo de encabezado Mapiform.h.</span><span class="sxs-lookup"><span data-stu-id="ff6e1-106">You are not required to use these macros, but if you do not, you should take particular care that your declarations conform to the declarations in the Mapiform.h header file.</span></span> <span data-ttu-id="ff6e1-107">Por ejemplo, podría declarar la clase de objeto de formulario del servidor de formulario como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="ff6e1-107">For example, you could declare your form server's form object class like the following:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="ff6e1-108">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff6e1-108">See also</span></span>



[<span data-ttu-id="ff6e1-109">Escritura de código de servidor de formulario</span><span class="sxs-lookup"><span data-stu-id="ff6e1-109">Writing Form Server Code</span></span>](writing-form-server-code.md)

