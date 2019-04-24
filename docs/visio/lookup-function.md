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
description: Devuelve un índice basado en cero que indica la ubicación de la clave de subcadena en una lista o devuelve-1 si la cadena de destino contiene el delimitador.
ms.openlocfilehash: 10fc32e6e979ab819246161dedfb1183c2683a99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358033"
---
# <a name="lookup-function"></a><span data-ttu-id="e4ffb-103">Función LOOKUP</span><span class="sxs-lookup"><span data-stu-id="e4ffb-103">LOOKUP Function</span></span>

<span data-ttu-id="e4ffb-104">Devuelve un índice basado en cero que indica la ubicación de la _clave_ de subcadena en una _lista_o devuelve-1 si la cadena de destino contiene __ el delimitador.</span><span class="sxs-lookup"><span data-stu-id="e4ffb-104">Returns a zero-based index that indicates the location of the substring  _key_ in a  _list_, or returns -1 if the target string contains the  _delimiter_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e4ffb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4ffb-105">Syntax</span></span>

<span data-ttu-id="e4ffb-106">Lookup ("\* \* *key* \* *", "* \* *List* \* *" [, "* \* \*\* delimitador \* \*"])</span><span class="sxs-lookup"><span data-stu-id="e4ffb-106">LOOKUP(" \*\* *key* \*\* "," \*\* *list* \*\* "[," \*\* *delimiter* \*\* "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e4ffb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4ffb-107">Parameters</span></span>

|<span data-ttu-id="e4ffb-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e4ffb-108">**Name**</span></span>|<span data-ttu-id="e4ffb-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e4ffb-109">**Required/Optional**</span></span>|<span data-ttu-id="e4ffb-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="e4ffb-110">**Data Type**</span></span>|<span data-ttu-id="e4ffb-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e4ffb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e4ffb-112">_key_</span><span class="sxs-lookup"><span data-stu-id="e4ffb-112">_key_</span></span> <br/> |<span data-ttu-id="e4ffb-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e4ffb-113">Required</span></span>  <br/> |<span data-ttu-id="e4ffb-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e4ffb-114">**String**</span></span> <br/> |<span data-ttu-id="e4ffb-115">Cadena que desea buscar.</span><span class="sxs-lookup"><span data-stu-id="e4ffb-115">The string that you want to look up.</span></span>  <br/> |
| <span data-ttu-id="e4ffb-116">_list_</span><span class="sxs-lookup"><span data-stu-id="e4ffb-116">_list_</span></span> <br/> |<span data-ttu-id="e4ffb-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e4ffb-117">Required</span></span>  <br/> |<span data-ttu-id="e4ffb-118">**String**</span><span class="sxs-lookup"><span data-stu-id="e4ffb-118">**String**</span></span> <br/> | <span data-ttu-id="e4ffb-119">Lista en la que desea realizar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e4ffb-119">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="e4ffb-120">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="e4ffb-120">_delimiter_</span></span> <br/> |<span data-ttu-id="e4ffb-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="e4ffb-121">Optional</span></span>  <br/> |<span data-ttu-id="e4ffb-122">**String**</span><span class="sxs-lookup"><span data-stu-id="e4ffb-122">**String**</span></span> <br/> | <span data-ttu-id="e4ffb-123">La cadena que se va a usar como delimitador de la _lista_.</span><span class="sxs-lookup"><span data-stu-id="e4ffb-123">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="e4ffb-124">Una __ cadena de delimitador puede tener más de un carácter de longitud y puede incluir caracteres de varios bytes.</span><span class="sxs-lookup"><span data-stu-id="e4ffb-124">A  _delimiter_ string can be more than one character in length and may include multibyte characters.</span></span> <span data-ttu-id="e4ffb-125">El valor predeterminado es un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="e4ffb-125">The default is a semicolon.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e4ffb-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4ffb-126">Return value</span></span>

<span data-ttu-id="e4ffb-127">Numeric</span><span class="sxs-lookup"><span data-stu-id="e4ffb-127">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e4ffb-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e4ffb-128">Remarks</span></span>

<span data-ttu-id="e4ffb-p102">La función LOOKUP utiliza un sistema de búsqueda que no diferencia mayúsculas y minúsculas. Si la lista comienza o termina con un delimitador, se supone que existe una cadena nula antes o después de la misma. Dos delimitadores consecutivos indican que hay una cadena nula entre ellos.</span><span class="sxs-lookup"><span data-stu-id="e4ffb-p102">The LOOKUP function uses a case-insensitive search. If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="e4ffb-p103">Todos los argumentos deben ser cadenas o expresiones que se puedan convertir en cadenas. En caso contrario, el argumento que no cumpla esa norma será reemplazado por una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="e4ffb-p103">All the arguments must be strings or expressions that can be converted to strings. If they are not, an empty string is substituted for the offending argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e4ffb-134">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4ffb-134">Example 1</span></span>

<span data-ttu-id="e4ffb-135">LOOKUP ("rata", "gato; rata;; caprino ")</span><span class="sxs-lookup"><span data-stu-id="e4ffb-135">LOOKUP("rat","cat;rat;;goat")</span></span>
  
<span data-ttu-id="e4ffb-136">Devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="e4ffb-136">Returns 1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e4ffb-137">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="e4ffb-137">Example 2</span></span>

<span data-ttu-id="e4ffb-138">BÚSQUEDA ("", "; cat; Rat;; caprino ")</span><span class="sxs-lookup"><span data-stu-id="e4ffb-138">LOOKUP("",";cat;rat;;goat")</span></span>
  
<span data-ttu-id="e4ffb-139">Devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="e4ffb-139">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e4ffb-140">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="e4ffb-140">Example 3</span></span>

<span data-ttu-id="e4ffb-141">LOOKUP ("t", "gato; Rat;; caprino "," a ")</span><span class="sxs-lookup"><span data-stu-id="e4ffb-141">LOOKUP("t","cat;rat;;goat","a")</span></span>
  
<span data-ttu-id="e4ffb-142">Devuelve 3.</span><span class="sxs-lookup"><span data-stu-id="e4ffb-142">Returns 3.</span></span>
  

