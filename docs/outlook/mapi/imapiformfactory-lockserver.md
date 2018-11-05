---
title: IMAPIFormFactoryLockServer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.LockServer
api_type:
- COM
ms.assetid: b9bd389a-6975-41a2-a2f4-e501312e434b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ab51b939651bc3c121f357545969d26832a19d19
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389060"
---
# <a name="imapiformfactorylockserver"></a><span data-ttu-id="4df24-103">IMAPIFormFactory::LockServer</span><span class="sxs-lookup"><span data-stu-id="4df24-103">IMAPIFormFactory::LockServer</span></span>

  
  
<span data-ttu-id="4df24-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4df24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4df24-105">Mantiene un servidor de formulario abierto en la memoria.</span><span class="sxs-lookup"><span data-stu-id="4df24-105">Keeps an open form server in memory.</span></span>
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a><span data-ttu-id="4df24-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="4df24-106">Parameters</span></span>

 <span data-ttu-id="4df24-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4df24-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4df24-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4df24-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4df24-109">_fLockServer_</span><span class="sxs-lookup"><span data-stu-id="4df24-109">_fLockServer_</span></span>
  
> <span data-ttu-id="4df24-110">[entrada] **true** para incrementar el recuento de bloqueos; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="4df24-110">[in] **true** to increment the lock count; otherwise, **false**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4df24-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4df24-111">Return value</span></span>

<span data-ttu-id="4df24-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="4df24-112">S_OK</span></span> 
  
> <span data-ttu-id="4df24-113">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="4df24-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4df24-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4df24-114">Remarks</span></span>

<span data-ttu-id="4df24-115">Visores de formulario llamar al método **IMAPIFormFactory::LockServer** para mantener una aplicación de servidor de formulario abierto en la memoria.</span><span class="sxs-lookup"><span data-stu-id="4df24-115">Form viewers call the **IMAPIFormFactory::LockServer** method to keep an open form server application in memory.</span></span> <span data-ttu-id="4df24-116">Mantener el servidor de formulario en la memoria mejora su rendimiento cuando los formularios se crean y se publicó con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="4df24-116">Keeping the form server in memory improves its performance when forms are frequently created and released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4df24-117">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="4df24-117">Notes to implementers</span></span>

<span data-ttu-id="4df24-118">El método **IMAPIFormFactory::LockServer** es muy similar al método [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4df24-118">The **IMAPIFormFactory::LockServer** method is very similar to the [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="4df24-119">Básicamente, el método **IMAPIFormFactory::LockServer** mantiene un recuento de cuántas veces se ha llamado; siempre y cuando ese count es mayor que 0, el método impide que el servidor de formulario se descarga de la memoria.</span><span class="sxs-lookup"><span data-stu-id="4df24-119">Essentially, the **IMAPIFormFactory::LockServer** method maintains a count of how many times it has been called; as long as that count is greater than 0, the method prevents the form server from being unloaded from memory.</span></span> <span data-ttu-id="4df24-120">Puede utilizar la función [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) para implementar esto.</span><span class="sxs-lookup"><span data-stu-id="4df24-120">You can use the [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) function to implement this.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4df24-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="4df24-121">See also</span></span>



[<span data-ttu-id="4df24-122">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4df24-122">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

