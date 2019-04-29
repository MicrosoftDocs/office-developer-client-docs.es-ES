---
title: Recuperar propiedades de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 023d2cf312438b1e4b6a90c57e1ead7d606d7727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412922"
---
# <a name="retrieving-form-properties"></a><span data-ttu-id="10802-103">Recuperar propiedades de formulario</span><span class="sxs-lookup"><span data-stu-id="10802-103">Retrieving Form Properties</span></span>

  
  
<span data-ttu-id="10802-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10802-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10802-105">Para emitir una consulta que sea significativa para un tipo de mensaje personalizado, una aplicación debe conocer las propiedades que se esperan en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="10802-105">To issue a query that is meaningful to a custom message type, an application needs to know the properties that are expected on that message.</span></span> <span data-ttu-id="10802-106">Para obtener una lista de las propiedades que usa una clase de mensaje personalizada, una aplicación cliente consulta el administrador de formularios MAPI.</span><span class="sxs-lookup"><span data-stu-id="10802-106">To get a list of properties that a custom message class uses, a client application queries the MAPI form manager.</span></span> <span data-ttu-id="10802-107">El administrador de formularios obtiene esta información del archivo de configuración de formulario apropiado para que las aplicaciones cliente puedan usar esta información sin la sobrecarga de activar el servidor de formularios en sí.</span><span class="sxs-lookup"><span data-stu-id="10802-107">The form manager gets this information from the appropriate form configuration file so that client applications can use this information without the overhead of activating the form server itself.</span></span> <span data-ttu-id="10802-108">Para ello, la aplicación cliente llama al método [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="10802-108">To do this, the client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method as follows:</span></span> 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

<span data-ttu-id="10802-109">Tenga en cuenta que el tercer argumento de **ResolveMessageClass** es la carpeta que contiene la tabla de contenido asociada en la que la consulta buscará los servidores de formularios.</span><span class="sxs-lookup"><span data-stu-id="10802-109">Note that the third argument to **ResolveMessageClass** is the folder that contains the associated contents table that the query will search for form servers.</span></span> <span data-ttu-id="10802-110">NULL indica que el administrador de formularios debe buscar en todos los contenedores de formularios disponibles.</span><span class="sxs-lookup"><span data-stu-id="10802-110">NULL indicates that the form manager should search all available form containers.</span></span> <span data-ttu-id="10802-111">Si la consulta se va a ejecutar en una carpeta determinada, es mejor incluir el puntero [IMAPIFolder](imapifolderimapicontainer.md) apropiado en su lugar.</span><span class="sxs-lookup"><span data-stu-id="10802-111">If the query is to run against a particular folder, it is better to include the appropriate [IMAPIFolder](imapifolderimapicontainer.md) pointer instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="10802-112">Ver también</span><span class="sxs-lookup"><span data-stu-id="10802-112">See also</span></span>



[<span data-ttu-id="10802-113">InterAcciones del servidor de formularios</span><span class="sxs-lookup"><span data-stu-id="10802-113">Form Server Interactions</span></span>](form-server-interactions.md)

