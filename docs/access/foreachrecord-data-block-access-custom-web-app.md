---
title: Bloque de datos ForEachRecord (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Un bloque de datos ForEachRecord repite un conjunto de instrucciones para cada registro de un dominio.
ms.openlocfilehash: 9715824bff7d478fa2880ada5e8770f7a0c88883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428238"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a><span data-ttu-id="71090-103">Bloque de datos ForEachRecord (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="71090-103">ForEachRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="71090-104">Un **bloque de datos ForEachRecord** repite un conjunto de instrucciones para cada registro de un dominio.</span><span class="sxs-lookup"><span data-stu-id="71090-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="71090-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="71090-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="71090-107">El bloque de datos **ParaCadaRegistro** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="71090-107">The **ForEachRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="71090-108">Configuración</span><span class="sxs-lookup"><span data-stu-id="71090-108">Setting</span></span>

<span data-ttu-id="71090-109">La acción **ParaCadaRegistro** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="71090-109">The **ForEachRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="71090-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="71090-110">**Argument name**</span></span>|<span data-ttu-id="71090-111">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="71090-111">**Required**</span></span>|<span data-ttu-id="71090-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="71090-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="71090-113">**In**</span><span class="sxs-lookup"><span data-stu-id="71090-113">**In**</span></span> <br/> |<span data-ttu-id="71090-114">Sí</span><span class="sxs-lookup"><span data-stu-id="71090-114">Yes</span></span>  <br/> |<span data-ttu-id="71090-115">Una cadena que identifica el dominio de los registros en los que se operará.</span><span class="sxs-lookup"><span data-stu-id="71090-115">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="71090-116">El *argumento In* puede contener el nombre de la tabla, una consulta select o una instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="71090-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> <span data-ttu-id="71090-117">**NOTA:** el dominio especificado no puede incluir datos almacenados en una tabla vinculada u origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="71090-117">**NOTE**: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span>           |
|<span data-ttu-id="71090-118">**Where Condition**</span><span class="sxs-lookup"><span data-stu-id="71090-118">**Where Condition**</span></span> <br/> |<span data-ttu-id="71090-119">No</span><span class="sxs-lookup"><span data-stu-id="71090-119">No</span></span>  <br/> |<span data-ttu-id="71090-120">Expresión de cadena usada para restringir el intervalo de datos en el que se realiza el bloque de datos **ForEachRecord.**</span><span class="sxs-lookup"><span data-stu-id="71090-120">A string expression used to restrict the range of data on which the **ForEachRecord** data block is performed.</span></span> <span data-ttu-id="71090-121">Por ejemplo, los criterios a menudo equivalen a la cláusula WHERE en una expresión SQL, sin la palabra WHERE.</span><span class="sxs-lookup"><span data-stu-id="71090-121">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="71090-122">Si se omiten criterios, el bloque de datos **ForEachRecord** funciona en todo el dominio especificado por el *argumento In.*</span><span class="sxs-lookup"><span data-stu-id="71090-122">If criteria are omitted, the **ForEachRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="71090-123">Cualquier campo que se incluya en criteria también debe ser un campo en  *In*  .</span><span class="sxs-lookup"><span data-stu-id="71090-123">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
|<span data-ttu-id="71090-124">**Alias**</span><span class="sxs-lookup"><span data-stu-id="71090-124">**Alias**</span></span> <br/> |<span data-ttu-id="71090-125">No</span><span class="sxs-lookup"><span data-stu-id="71090-125">No</span></span>  <br/> |<span data-ttu-id="71090-126">Cadena que proporciona un nombre alternativo para el dominio especificado por el *argumento In.*</span><span class="sxs-lookup"><span data-stu-id="71090-126">A string that provides an alternative name for the domain specified by the  *In*  argument.</span></span> <span data-ttu-id="71090-127">Se utiliza a menudo para acortar el nombre de la tabla en referencias posteriores con el fin de evitar posibles referencias ambiguas.</span><span class="sxs-lookup"><span data-stu-id="71090-127">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="71090-128">Si no se especifica  *Alias,*  se usará el nombre de la tabla o consulta como alias.</span><span class="sxs-lookup"><span data-stu-id="71090-128">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71090-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="71090-129">Remarks</span></span>

<span data-ttu-id="71090-130">Utilice la acción **[SalirDeCadaRegistro](exitforeachrecord-macro-action-access-custom-web-app.md)** para salir inmediatamente de un bloque de datos **ParaCadaRegistro**.</span><span class="sxs-lookup"><span data-stu-id="71090-130">Use the **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** action to exit a **ForEachRecord** data block immediately.</span></span> 
  

