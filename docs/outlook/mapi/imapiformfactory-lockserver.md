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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342143"
---
# <a name="imapiformfactorylockserver"></a><span data-ttu-id="ee174-103">IMAPIFormFactory::LockServer</span><span class="sxs-lookup"><span data-stu-id="ee174-103">IMAPIFormFactory::LockServer</span></span>

  
  
<span data-ttu-id="ee174-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee174-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee174-105">Mantiene un servidor de formulario abierto en la memoria.</span><span class="sxs-lookup"><span data-stu-id="ee174-105">Keeps an open form server in memory.</span></span>
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a><span data-ttu-id="ee174-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ee174-106">Parameters</span></span>

 <span data-ttu-id="ee174-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee174-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ee174-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ee174-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ee174-109">_fLockServer_</span><span class="sxs-lookup"><span data-stu-id="ee174-109">_fLockServer_</span></span>
  
> <span data-ttu-id="ee174-110">a **true** para incrementar el recuento de bloqueos; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="ee174-110">[in] **true** to increment the lock count; otherwise, **false**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ee174-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee174-111">Return value</span></span>

<span data-ttu-id="ee174-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee174-112">S_OK</span></span> 
  
> <span data-ttu-id="ee174-113">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="ee174-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee174-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ee174-114">Remarks</span></span>

<span data-ttu-id="ee174-115">Los visores de formularios llaman al método **IMAPIFormFactory:: LockServer** para mantener una aplicación de servidor de formulario abierta en la memoria.</span><span class="sxs-lookup"><span data-stu-id="ee174-115">Form viewers call the **IMAPIFormFactory::LockServer** method to keep an open form server application in memory.</span></span> <span data-ttu-id="ee174-116">Mantener el servidor de formularios en la memoria mejora el rendimiento cuando los formularios se crean y se publican con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="ee174-116">Keeping the form server in memory improves its performance when forms are frequently created and released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ee174-117">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="ee174-117">Notes to implementers</span></span>

<span data-ttu-id="ee174-118">El método **IMAPIFormFactory:: LockServer** es muy similar al método [IClassFactory:: LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ee174-118">The **IMAPIFormFactory::LockServer** method is very similar to the [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="ee174-119">Básicamente, el método **IMAPIFormFactory:: LockServer** mantiene un recuento de cuántas veces se ha llamado; siempre que el recuento sea mayor que 0, el método impide que el servidor de formularios se descargue de la memoria.</span><span class="sxs-lookup"><span data-stu-id="ee174-119">Essentially, the **IMAPIFormFactory::LockServer** method maintains a count of how many times it has been called; as long as that count is greater than 0, the method prevents the form server from being unloaded from memory.</span></span> <span data-ttu-id="ee174-120">Puede usar la función [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) para implementar esto.</span><span class="sxs-lookup"><span data-stu-id="ee174-120">You can use the [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) function to implement this.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee174-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee174-121">See also</span></span>



[<span data-ttu-id="ee174-122">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee174-122">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

