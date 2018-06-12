---
title: LOOKUP (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251457
localization_priority: Normal
ms.assetid: cb6ec664-6062-75d0-1514-8058b98c2c36
description: Devuelve un índice de base cero que indica la ubicación de la subcadena clave en una lista o devuelve -1 si la cadena de destino contiene el delimitador.
ms.openlocfilehash: e1fd433282871135d385d1c980c77041cd49cdf4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822554"
---
# <a name="lookup-function"></a><span data-ttu-id="5557c-103">LOOKUP (función)</span><span class="sxs-lookup"><span data-stu-id="5557c-103">LOOKUP Function</span></span>

<span data-ttu-id="5557c-104">Devuelve un índice de base cero que indica la ubicación de la subcadena _clave_ en una _lista_o devuelve -1 si la cadena de destino contiene el _delimitador_.</span><span class="sxs-lookup"><span data-stu-id="5557c-104">Returns a zero-based index that indicates the location of the substring  _key_ in a  _list_, or returns -1 if the target string contains the  _delimiter_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5557c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5557c-105">Syntax</span></span>

<span data-ttu-id="5557c-106">BÚSQUEDA ("** *clave* **","** *lista* **"["," ** *delimitador* ** "])</span><span class="sxs-lookup"><span data-stu-id="5557c-106">LOOKUP(" ** *key* ** "," ** *list* ** "[," ** *delimiter* ** "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5557c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5557c-107">Parameters</span></span>

|<span data-ttu-id="5557c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5557c-108">**Name**</span></span>|<span data-ttu-id="5557c-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="5557c-109">**Required/Optional**</span></span>|<span data-ttu-id="5557c-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="5557c-110">**Data Type**</span></span>|<span data-ttu-id="5557c-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5557c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5557c-112">_clave_</span><span class="sxs-lookup"><span data-stu-id="5557c-112">_key_</span></span> <br/> |<span data-ttu-id="5557c-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5557c-113">Required</span></span>  <br/> |<span data-ttu-id="5557c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5557c-114">**String**</span></span> <br/> |<span data-ttu-id="5557c-115">Cadena que desea buscar.</span><span class="sxs-lookup"><span data-stu-id="5557c-115">The string that you want to look up.</span></span>  <br/> |
| <span data-ttu-id="5557c-116">_lista_</span><span class="sxs-lookup"><span data-stu-id="5557c-116">_list_</span></span> <br/> |<span data-ttu-id="5557c-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5557c-117">Required</span></span>  <br/> |<span data-ttu-id="5557c-118">**String**</span><span class="sxs-lookup"><span data-stu-id="5557c-118">**String**</span></span> <br/> | <span data-ttu-id="5557c-119">Lista en la que desea realizar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5557c-119">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="5557c-120">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="5557c-120">_delimiter_</span></span> <br/> |<span data-ttu-id="5557c-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="5557c-121">Optional</span></span>  <br/> |<span data-ttu-id="5557c-122">**String**</span><span class="sxs-lookup"><span data-stu-id="5557c-122">**String**</span></span> <br/> | <span data-ttu-id="5557c-123">La cadena que se utilizará como delimitador en _lista_.</span><span class="sxs-lookup"><span data-stu-id="5557c-123">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="5557c-124">Una cadena _delimitador_ puede tener más de un carácter de longitud y puede incluir caracteres con múltiples bytes.</span><span class="sxs-lookup"><span data-stu-id="5557c-124">A  _delimiter_ string can be more than one character in length and may include multibyte characters.</span></span> <span data-ttu-id="5557c-125">El valor predeterminado es un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="5557c-125">The default is a semicolon.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5557c-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5557c-126">Return value</span></span>

<span data-ttu-id="5557c-127">Numeric</span><span class="sxs-lookup"><span data-stu-id="5557c-127">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5557c-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5557c-128">Remarks</span></span>

<span data-ttu-id="5557c-p102">La función LOOKUP utiliza un sistema de búsqueda que no diferencia mayúsculas y minúsculas. Si la lista comienza o termina con un delimitador, se supone que existe una cadena nula antes o después de la misma. Dos delimitadores consecutivos indican que hay una cadena nula entre ellos.</span><span class="sxs-lookup"><span data-stu-id="5557c-p102">The LOOKUP function uses a case-insensitive search. If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="5557c-p103">Todos los argumentos deben ser cadenas o expresiones que se puedan convertir en cadenas. En caso contrario, el argumento que no cumpla esa norma será reemplazado por una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="5557c-p103">All the arguments must be strings or expressions that can be converted to strings. If they are not, an empty string is substituted for the offending argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="5557c-134">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="5557c-134">Example 1</span></span>

<span data-ttu-id="5557c-135">LOOKUP("rata","gato;rata;;cabra")</span><span class="sxs-lookup"><span data-stu-id="5557c-135">LOOKUP("rat","cat;rat;;goat")</span></span>
  
<span data-ttu-id="5557c-136">Devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="5557c-136">Returns 1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="5557c-137">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="5557c-137">Example 2</span></span>

<span data-ttu-id="5557c-138">LOOKUP("";";gato;rata;;cabra")</span><span class="sxs-lookup"><span data-stu-id="5557c-138">LOOKUP("",";cat;rat;;goat")</span></span>
  
<span data-ttu-id="5557c-139">Devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="5557c-139">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="5557c-140">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="5557c-140">Example 3</span></span>

<span data-ttu-id="5557c-141">LOOKUP("t","gato;rata;;pato","a")</span><span class="sxs-lookup"><span data-stu-id="5557c-141">LOOKUP("t","cat;rat;;goat","a")</span></span>
  
<span data-ttu-id="5557c-142">Devuelve 3.</span><span class="sxs-lookup"><span data-stu-id="5557c-142">Returns 3.</span></span>
  

