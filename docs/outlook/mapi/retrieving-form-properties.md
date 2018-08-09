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
ms.openlocfilehash: 334ecaacec88c3730f4cc2f4c80eb35d5a553c4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820532"
---
# <a name="retrieving-form-properties"></a><span data-ttu-id="45b04-103">Recuperar propiedades de formulario</span><span class="sxs-lookup"><span data-stu-id="45b04-103">Retrieving Form Properties</span></span>

  
  
<span data-ttu-id="45b04-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45b04-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45b04-105">Para ejecutar una consulta que sea significativa para un tipo de mensaje personalizado, una aplicación necesita conocer las propiedades que se esperan en ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="45b04-105">To issue a query that is meaningful to a custom message type, an application needs to know the properties that are expected on that message.</span></span> <span data-ttu-id="45b04-106">Para obtener una lista de propiedades que usa una clase de mensaje personalizada, una aplicación cliente consulta el Administrador de formularios de MAPI.</span><span class="sxs-lookup"><span data-stu-id="45b04-106">To get a list of properties that a custom message class uses, a client application queries the MAPI form manager.</span></span> <span data-ttu-id="45b04-107">El Administrador de formulario obtiene esta información desde el archivo de configuración de forma adecuada para que las aplicaciones cliente pueden usar esta información sin la sobrecarga de activar el formulario del propio servidor.</span><span class="sxs-lookup"><span data-stu-id="45b04-107">The form manager gets this information from the appropriate form configuration file so that client applications can use this information without the overhead of activating the form server itself.</span></span> <span data-ttu-id="45b04-108">Para ello, la aplicación cliente llama al método [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="45b04-108">To do this, the client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method as follows:</span></span> 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

<span data-ttu-id="45b04-109">Tenga en cuenta que el tercer argumento para **ResolveMessageClass** es la carpeta que contiene la tabla de contenido asociada que la consulta buscará los servidores del formulario.</span><span class="sxs-lookup"><span data-stu-id="45b04-109">Note that the third argument to **ResolveMessageClass** is the folder that contains the associated contents table that the query will search for form servers.</span></span> <span data-ttu-id="45b04-110">NULL indica que el Administrador de formulario debe buscar en todos los contenedores de formulario disponibles.</span><span class="sxs-lookup"><span data-stu-id="45b04-110">NULL indicates that the form manager should search all available form containers.</span></span> <span data-ttu-id="45b04-111">Si la consulta es ejecutar en una carpeta determinada, es mejor incluir el puntero [IMAPIFolder](imapifolderimapicontainer.md) apropiado en su lugar.</span><span class="sxs-lookup"><span data-stu-id="45b04-111">If the query is to run against a particular folder, it is better to include the appropriate [IMAPIFolder](imapifolderimapicontainer.md) pointer instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="45b04-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="45b04-112">See also</span></span>



[<span data-ttu-id="45b04-113">Interacciones del servidor de formulario</span><span class="sxs-lookup"><span data-stu-id="45b04-113">Form Server Interactions</span></span>](form-server-interactions.md)

