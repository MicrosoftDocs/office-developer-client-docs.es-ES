---
title: Bloque de datos LookupRecord (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Un bloque de datos BuscarRegistro realiza un conjunto de acciones en un registro específico.
ms.openlocfilehash: a6d89b1700a47f88086fd8c4e7b594b90425912c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434364"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a><span data-ttu-id="e49d8-103">Bloque de datos LookupRecord (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="e49d8-103">LookupRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="e49d8-104">Un bloque de datos **BuscarRegistro** realiza un conjunto de acciones en un registro específico.</span><span class="sxs-lookup"><span data-stu-id="e49d8-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e49d8-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="e49d8-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e49d8-107">El bloque de datos **BuscarRegistro** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="e49d8-107">The **LookupRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="e49d8-108">Setting</span><span class="sxs-lookup"><span data-stu-id="e49d8-108">Setting</span></span>

<span data-ttu-id="e49d8-109">La acción **EstablecerCampo** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="e49d8-109">The **SetField** action has the following arguments.</span></span> 
  
|<span data-ttu-id="e49d8-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="e49d8-110">**Argument**</span></span>|<span data-ttu-id="e49d8-111">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="e49d8-111">**Required**</span></span>|<span data-ttu-id="e49d8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e49d8-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e49d8-113">_A_</span><span class="sxs-lookup"><span data-stu-id="e49d8-113">_In_</span></span> <br/> |<span data-ttu-id="e49d8-114">Sí</span><span class="sxs-lookup"><span data-stu-id="e49d8-114">Yes</span></span>  <br/> |<span data-ttu-id="e49d8-115">Una cadena que identifica el registro en el que se operará.</span><span class="sxs-lookup"><span data-stu-id="e49d8-115">A string that identifies the record to operate on.</span></span> <span data-ttu-id="e49d8-116">El argumento *in* puede contener el nombre de la tabla, una consulta de selección o una instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="e49d8-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> |
| <span data-ttu-id="e49d8-117">_Where Condition_</span><span class="sxs-lookup"><span data-stu-id="e49d8-117">_Where Condition_</span></span> <br/> |<span data-ttu-id="e49d8-118">No</span><span class="sxs-lookup"><span data-stu-id="e49d8-118">No</span></span>  <br/> |<span data-ttu-id="e49d8-119">Una expresión de cadena que se utiliza para restringir el intervalo de datos en el que se ejecuta el bloque de datos **BuscarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="e49d8-119">A string expression used to restrict the range of data on which the **LookupRecord** data block is performed.</span></span> <span data-ttu-id="e49d8-120">Por ejemplo, los criterios a menudo equivalen a la cláusula WHERE en una expresión SQL, sin la palabra WHERE.</span><span class="sxs-lookup"><span data-stu-id="e49d8-120">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="e49d8-121">Si se omite criteria, el bloque de datos **LookupRecord** opera en todo el dominio especificado por el argumento *in* .</span><span class="sxs-lookup"><span data-stu-id="e49d8-121">If criteria is omitted, the **LookupRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="e49d8-122">Cualquier campo que se incluya en Criteria también debe ser un campo en *en* .</span><span class="sxs-lookup"><span data-stu-id="e49d8-122">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
| <span data-ttu-id="e49d8-123">_Alias_</span><span class="sxs-lookup"><span data-stu-id="e49d8-123">_Alias_</span></span> <br/> |<span data-ttu-id="e49d8-124">No</span><span class="sxs-lookup"><span data-stu-id="e49d8-124">No</span></span>  <br/> |<span data-ttu-id="e49d8-125">Una cadena que proporciona un nombre alternativo para el registro especificado por el argumento *in* .</span><span class="sxs-lookup"><span data-stu-id="e49d8-125">A string that provides an alternative name for the record specified by the  *In*  argument.</span></span> <span data-ttu-id="e49d8-126">Se utiliza a menudo para acortar el nombre de la tabla en referencias posteriores con el fin de evitar posibles referencias ambiguas.</span><span class="sxs-lookup"><span data-stu-id="e49d8-126">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="e49d8-127">Si no se especifica ningún *alias* , se utilizará el nombre de la tabla o consulta como alias.</span><span class="sxs-lookup"><span data-stu-id="e49d8-127">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e49d8-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e49d8-128">Remarks</span></span>

<span data-ttu-id="e49d8-129">Si los criterios especificados por los argumentos  *En*  y  *Condición WHERE*  especifican más de un registro, el bloque de datos **BuscarRegistro** solo operará en el primer registro.</span><span class="sxs-lookup"><span data-stu-id="e49d8-129">If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record.</span></span> 
  
<span data-ttu-id="e49d8-130">Si ningún registro cumple la *Condición Where* o si *en* no contiene registros, **LookupRecord** crea un registro en blanco en el que todos los campos contienen un valor **null** .</span><span class="sxs-lookup"><span data-stu-id="e49d8-130">If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value.</span></span> 
  

