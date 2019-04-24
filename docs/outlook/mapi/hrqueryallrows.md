---
title: HrQueryAllRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrQueryAllRows
api_type:
- HeaderDef
ms.assetid: b08fadcf-cdf3-48b7-9489-d7f745266482
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0f09304f21180d9ebc2a1e1dcc54ebadd3622804
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348247"
---
# <a name="hrqueryallrows"></a><span data-ttu-id="ec029-103">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="ec029-103">HrQueryAllRows</span></span>

  
  
<span data-ttu-id="ec029-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec029-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec029-105">Recupera todas las filas de una tabla.</span><span class="sxs-lookup"><span data-stu-id="ec029-105">Retrieves all rows of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ec029-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ec029-106">Header file:</span></span>  <br/> |<span data-ttu-id="ec029-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="ec029-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ec029-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="ec029-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ec029-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ec029-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ec029-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ec029-110">Called by:</span></span>  <br/> |<span data-ttu-id="ec029-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="ec029-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrQueryAllRows(
  LPMAPITABLE ptable,
  LPSPropTagArray ptaga,
  LPSRestriction pres,
  LPSSortOrderSet psos,
  LONG crowsMax,
  LPSRowSet FAR * pprows
);
```

## <a name="parameters"></a><span data-ttu-id="ec029-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="ec029-112">Parameters</span></span>

 <span data-ttu-id="ec029-113">_ptable_</span><span class="sxs-lookup"><span data-stu-id="ec029-113">_ptable_</span></span>
  
> <span data-ttu-id="ec029-114">a Puntero a la tabla MAPI desde la que se recuperan las filas.</span><span class="sxs-lookup"><span data-stu-id="ec029-114">[in] Pointer to the MAPI table from which rows are retrieved.</span></span> 
    
 <span data-ttu-id="ec029-115">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="ec029-115">_ptaga_</span></span>
  
> <span data-ttu-id="ec029-116">a Puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indica las columnas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="ec029-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating table columns.</span></span> <span data-ttu-id="ec029-117">Estas etiquetas se usan para seleccionar las columnas específicas que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="ec029-117">These tags are used to select the specific columns to be retrieved.</span></span> <span data-ttu-id="ec029-118">Si el parámetro _ptaga_ es null, **HrQueryAllRows** recupera todo el conjunto de columnas de la vista de tabla actual pasada en el parámetro _ptable_ .</span><span class="sxs-lookup"><span data-stu-id="ec029-118">If the  _ptaga_ parameter is NULL, **HrQueryAllRows** retrieves the entire column set of the current table view passed in the  _ptable_ parameter.</span></span> 
    
 <span data-ttu-id="ec029-119">_impresa_</span><span class="sxs-lookup"><span data-stu-id="ec029-119">_pres_</span></span>
  
> <span data-ttu-id="ec029-120">a Puntero a una estructura [SRestriction](srestriction.md) que contiene restricciones de recuperación.</span><span class="sxs-lookup"><span data-stu-id="ec029-120">[in] Pointer to an [SRestriction](srestriction.md) structure that contains retrieval restrictions.</span></span> <span data-ttu-id="ec029-121">Si el parámetro _Pres_ es null, **HrQueryAllRows** no realiza ninguna restricción.</span><span class="sxs-lookup"><span data-stu-id="ec029-121">If the  _pres_ parameter is NULL, **HrQueryAllRows** makes no restrictions.</span></span> 
    
 <span data-ttu-id="ec029-122">_PSO_</span><span class="sxs-lookup"><span data-stu-id="ec029-122">_psos_</span></span>
  
> <span data-ttu-id="ec029-123">a Puntero a una estructura [SSortOrderSet](ssortorderset.md) que identifica el criterio de ordenación de las columnas que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="ec029-123">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order of the columns to be retrieved.</span></span> <span data-ttu-id="ec029-124">Si el parámetro _PSO_ es null, se usa el criterio de ordenación predeterminado para la tabla.</span><span class="sxs-lookup"><span data-stu-id="ec029-124">If the  _psos_ parameter is NULL, the default sort order for the table is used.</span></span> 
    
 <span data-ttu-id="ec029-125">_crowsMax_</span><span class="sxs-lookup"><span data-stu-id="ec029-125">_crowsMax_</span></span>
  
> <span data-ttu-id="ec029-126">a Número máximo de filas que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="ec029-126">[in] Maximum number of rows to be retrieved.</span></span> <span data-ttu-id="ec029-127">Si el valor del parámetro _crowsMax_ es cero, no se establece ningún límite en el número de filas recuperadas.</span><span class="sxs-lookup"><span data-stu-id="ec029-127">If the value of the  _crowsMax_ parameter is zero, no limit on the number of rows retrieved is set.</span></span> 
    
 <span data-ttu-id="ec029-128">_ppRows_</span><span class="sxs-lookup"><span data-stu-id="ec029-128">_pprows_</span></span>
  
> <span data-ttu-id="ec029-129">contempla Puntero a un puntero a la estructura [SRowSet](srowset.md) devuelta que contiene una matriz de punteros a las filas de tabla recuperadas.</span><span class="sxs-lookup"><span data-stu-id="ec029-129">[out] Pointer to a pointer to the returned [SRowSet](srowset.md) structure that contains an array of pointers to the retrieved table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ec029-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec029-130">Return value</span></span>

<span data-ttu-id="ec029-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec029-131">S_OK</span></span> 
  
> <span data-ttu-id="ec029-132">La llamada recuperó las filas esperadas de una tabla.</span><span class="sxs-lookup"><span data-stu-id="ec029-132">The call retrieved the expected rows of a table.</span></span> 
    
<span data-ttu-id="ec029-133">MAPI_E_TABLE_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="ec029-133">MAPI_E_TABLE_TOO_BIG</span></span> 
  
> <span data-ttu-id="ec029-134">El número de filas de la tabla es mayor que el número pasado para el parámetro _crowsMax_ .</span><span class="sxs-lookup"><span data-stu-id="ec029-134">The number of rows in the table is larger than the number passed for the  _crowsMax_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ec029-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ec029-135">Remarks</span></span>

<span data-ttu-id="ec029-136">Una aplicación cliente o un proveedor de servicios no tiene control sobre el número de filas que **HrQueryAllRows** intenta recuperar, a excepción de la imposición de una restricción a la que apunta el parámetro _Pres_ .</span><span class="sxs-lookup"><span data-stu-id="ec029-136">A client application or service provider has no control over the number of rows **HrQueryAllRows** attempts to retrieve, other than by imposing a restriction pointed to by the  _pres_ parameter.</span></span> <span data-ttu-id="ec029-137">El parámetro _crowsMax_ no limita la recuperación a un número determinado de filas de tabla, sino que define una cantidad máxima de memoria disponible para contener todas las filas recuperadas.</span><span class="sxs-lookup"><span data-stu-id="ec029-137">The  _crowsMax_ parameter does not limit the retrieval to a certain number of table rows, but rather defines a maximum amount of memory available to hold all retrieved rows.</span></span> <span data-ttu-id="ec029-138">La única protección contra el desbordamiento de memoria masivo es la característica provisional que proporciona la configuración de _crowsMax_.</span><span class="sxs-lookup"><span data-stu-id="ec029-138">The only protection against massive memory overflow is the stopgap feature provided by setting  _crowsMax_.</span></span> <span data-ttu-id="ec029-139">El MAPI_E_TABLE_TOO_BIG de devolución de error significa que la tabla contiene demasiadas filas que se mantendrán todas a la vez en la memoria.</span><span class="sxs-lookup"><span data-stu-id="ec029-139">The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be held all at once in memory.</span></span> 
  
<span data-ttu-id="ec029-140">Normalmente, las tablas pequeñas, como una tabla de almacén de mensajes o una tabla de proveedor, se pueden recuperar con seguridad con **HrQueryAllRows**.</span><span class="sxs-lookup"><span data-stu-id="ec029-140">Tables that are typically small, such as a message store table or a provider table, usually can be safely retrieved with **HrQueryAllRows**.</span></span> <span data-ttu-id="ec029-141">Las tablas con riesgo de ser muy grandes, como una tabla de contenido o incluso una tabla de destinatarios, deben atravesarse en subsecciones mediante el método [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="ec029-141">Tables at risk of being very large, such as a contents table or even a recipients table, should be traversed in subsections using the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> 
  
<span data-ttu-id="ec029-142">Si no se define ninguna propiedad de la tabla cuando se llama a **HrQueryAllRows** , se devuelven con el tipo de propiedad PT_NULL y el identificador de propiedad PROP_ID_NULL</span><span class="sxs-lookup"><span data-stu-id="ec029-142">If any table properties are undefined when **HrQueryAllRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL</span></span> 
  

