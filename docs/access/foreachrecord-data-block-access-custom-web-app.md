---
title: Bloque de datos ParaCadaRegistro (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Un bloque de datos ParaCadaRegistro repite un conjunto de instrucciones para cada registro en un dominio.
ms.openlocfilehash: 8ad14a01be05de9fb34299e49a9737f2009ef5ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815344"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a><span data-ttu-id="26539-103">Bloque de datos ParaCadaRegistro (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="26539-103">ForEachRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="26539-104">Un bloque de datos **ParaCadaRegistro** repite un conjunto de instrucciones para cada registro en un dominio.</span><span class="sxs-lookup"><span data-stu-id="26539-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="26539-p101">[!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="26539-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="26539-107">[!NOTA] El bloque de datos **ParaCadaRegistro** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="26539-107">The **ForEachRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="26539-108">Valores</span><span class="sxs-lookup"><span data-stu-id="26539-108">Setting</span></span>

<span data-ttu-id="26539-109">La acción **ParaCadaRegistro** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="26539-109">The **ForEachRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="26539-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="26539-110">**Argument name**</span></span>|<span data-ttu-id="26539-111">**Necesario**</span><span class="sxs-lookup"><span data-stu-id="26539-111">**Required**</span></span>|<span data-ttu-id="26539-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26539-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="26539-113">**En**</span><span class="sxs-lookup"><span data-stu-id="26539-113">**In**</span></span> <br/> |<span data-ttu-id="26539-114">Sí</span><span class="sxs-lookup"><span data-stu-id="26539-114">Yes</span></span>  <br/> |<span data-ttu-id="26539-115">Una cadena que identifica el dominio de registros que se va a funcionar en.</span><span class="sxs-lookup"><span data-stu-id="26539-115">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="26539-116">El argumento *en* puede contener el nombre de la tabla, una consulta de selección o una instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="26539-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> <span data-ttu-id="26539-117">**Nota**: el dominio especificado no puede incluir datos almacenados en una tabla vinculada u origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="26539-117">**NOTE**: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span>           |
|<span data-ttu-id="26539-118">**Where Condition**</span><span class="sxs-lookup"><span data-stu-id="26539-118">**Where Condition**</span></span> <br/> |<span data-ttu-id="26539-119">No</span><span class="sxs-lookup"><span data-stu-id="26539-119">No</span></span>  <br/> |<span data-ttu-id="26539-120">Expresión de cadena utilizada para restringir el intervalo de datos en la que el bloque de datos **ParaCadaRegistro** se lleva a cabo.</span><span class="sxs-lookup"><span data-stu-id="26539-120">A string expression used to restrict the range of data on which the **ForEachRecord** data block is performed.</span></span> <span data-ttu-id="26539-121">Por ejemplo, criterios con frecuencia es equivalente a la cláusula WHERE en una expresión SQL, sin la palabra donde.</span><span class="sxs-lookup"><span data-stu-id="26539-121">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="26539-122">Si se omiten criterios, el bloque de datos **ParaCadaRegistro** funciona en todo el dominio especificado por el argumento *en* .</span><span class="sxs-lookup"><span data-stu-id="26539-122">If criteria are omitted, the **ForEachRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="26539-123">Cualquier campo que se incluya en criterios debe ser también un campo de *en* .</span><span class="sxs-lookup"><span data-stu-id="26539-123">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
|<span data-ttu-id="26539-124">**Alias**</span><span class="sxs-lookup"><span data-stu-id="26539-124">**Alias**</span></span> <br/> |<span data-ttu-id="26539-125">No</span><span class="sxs-lookup"><span data-stu-id="26539-125">No</span></span>  <br/> |<span data-ttu-id="26539-126">Una cadena que proporciona un nombre alternativo para el dominio especificado por el argumento *en* .</span><span class="sxs-lookup"><span data-stu-id="26539-126">A string that provides an alternative name for the domain specified by the  *In*  argument.</span></span> <span data-ttu-id="26539-127">A menudo se usa para acortar el nombre de tabla para las referencias subsiguientes a fin de evitar posibles referencias ambiguas.</span><span class="sxs-lookup"><span data-stu-id="26539-127">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="26539-128">Si no se especifica el *Alias* , se usará el nombre de la tabla o consulta como el alias.</span><span class="sxs-lookup"><span data-stu-id="26539-128">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26539-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26539-129">Remarks</span></span>

<span data-ttu-id="26539-130">Utilice la acción **[SalirDeCadaRegistro](exitforeachrecord-macro-action-access-custom-web-app.md)** para salir inmediatamente de un bloque de datos **ParaCadaRegistro**.</span><span class="sxs-lookup"><span data-stu-id="26539-130">Use the **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** action to exit a **ForEachRecord** data block immediately.</span></span> 
  

