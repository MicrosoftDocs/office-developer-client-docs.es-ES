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
# <a name="declaring-form-interfaces"></a><span data-ttu-id="de43c-103">Declarar interfaces de formulario</span><span class="sxs-lookup"><span data-stu-id="de43c-103">Declaring Form Interfaces</span></span>

  
  
<span data-ttu-id="de43c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="de43c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="de43c-105">Las declaraciones de las implementaciones de interfaces de formulario MAPI se pueden simplificar mediante el uso de las macros de _interface__METHOD MAPI_, donde _interfaz_ es una interfaz de formulario definida en el archivo de encabezado Mapiform.h.</span><span class="sxs-lookup"><span data-stu-id="de43c-105">You can simplify the declarations of your implementations of MAPI form interfaces by using the MAPI_ _interface__METHOD macros, where  _interface_ is a form interface defined in the Mapiform.h header file.</span></span> <span data-ttu-id="de43c-106">No es necesario usar estas macros, pero si no lo hace, debe tener especial cuidado que las declaraciones de cumplir con las declaraciones en el archivo de encabezado Mapiform.h.</span><span class="sxs-lookup"><span data-stu-id="de43c-106">You are not required to use these macros, but if you do not, you should take particular care that your declarations conform to the declarations in the Mapiform.h header file.</span></span> <span data-ttu-id="de43c-107">Por ejemplo, podría declarar la clase de objeto de formulario de su servidor de forma similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="de43c-107">For example, you could declare your form server's form object class like the following:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="de43c-108">Vea también</span><span class="sxs-lookup"><span data-stu-id="de43c-108">See also</span></span>



[<span data-ttu-id="de43c-109">Escribir código de servidor de formulario</span><span class="sxs-lookup"><span data-stu-id="de43c-109">Writing Form Server Code</span></span>](writing-form-server-code.md)

