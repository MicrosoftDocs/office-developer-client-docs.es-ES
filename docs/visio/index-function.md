---
title: INDEX (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251443
localization_priority: Normal
ms.assetid: cc46f91e-733f-e25a-17d2-19df8c8febd2
description: Devuelve la subcadena en el índice de la ubicación de base cero de la lista delimitada por el delimitador. O bien, si el índice está fuera del intervalo, devuelve una cadena vacía o el token opcional proporcionado como el argumento valorDeError.
ms.openlocfilehash: b801f3b2a762f7767f32953806178be3eb264398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822329"
---
# <a name="index-function"></a><span data-ttu-id="4687c-104">Función INDEX</span><span class="sxs-lookup"><span data-stu-id="4687c-104">INDEX Function</span></span>

<span data-ttu-id="4687c-105">Devuelve la subcadena en la ubicación de base cero _índice_ en la _lista_ delimitada por el _delimitador_.</span><span class="sxs-lookup"><span data-stu-id="4687c-105">Returns the substring at the zero-based location  _index_ in the  _list_ delimited by  _delimiter_.</span></span> <span data-ttu-id="4687c-106">O bien, si el índice está fuera del intervalo, devuelve una cadena vacía o el token opcional proporcionado como el argumento *valorDeError* .</span><span class="sxs-lookup"><span data-stu-id="4687c-106">Or, if the index is out of range, returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4687c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4687c-107">Syntax</span></span>

<span data-ttu-id="4687c-108">ÍNDICE (** *índice* **, "** *lista* **" [, [** *delimitador* **] [, [** *valorDeError* **]]])</span><span class="sxs-lookup"><span data-stu-id="4687c-108">INDEX(** *index* **," ** *list* ** "[,[ ** *delimiter* ** ][,[ ** *errorvalue* ** ]]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4687c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4687c-109">Parameters</span></span>

|<span data-ttu-id="4687c-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="4687c-110">**Name**</span></span>|<span data-ttu-id="4687c-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="4687c-111">**Required/Optional**</span></span>|<span data-ttu-id="4687c-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4687c-112">**Data Type**</span></span>|<span data-ttu-id="4687c-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4687c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4687c-114">_index_</span><span class="sxs-lookup"><span data-stu-id="4687c-114">_index_</span></span> <br/> |<span data-ttu-id="4687c-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4687c-115">Required</span></span>  <br/> |<span data-ttu-id="4687c-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="4687c-116">**Number**</span></span> <br/> |<span data-ttu-id="4687c-117">Especifica la ubicación que desea buscar.</span><span class="sxs-lookup"><span data-stu-id="4687c-117">The location that you want to find.</span></span>  <br/> |
| <span data-ttu-id="4687c-118">_lista_</span><span class="sxs-lookup"><span data-stu-id="4687c-118">_list_</span></span> <br/> |<span data-ttu-id="4687c-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4687c-119">Required</span></span>  <br/> |<span data-ttu-id="4687c-120">**String**</span><span class="sxs-lookup"><span data-stu-id="4687c-120">**String**</span></span> <br/> |<span data-ttu-id="4687c-121">Lista en la que desea realizar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4687c-121">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="4687c-122">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="4687c-122">_delimiter_</span></span> <br/> |<span data-ttu-id="4687c-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="4687c-123">Optional</span></span>  <br/> |<span data-ttu-id="4687c-124">**String**</span><span class="sxs-lookup"><span data-stu-id="4687c-124">**String**</span></span> <br/> | <span data-ttu-id="4687c-125">La cadena que se utilizará como delimitador en _lista_.</span><span class="sxs-lookup"><span data-stu-id="4687c-125">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="4687c-126">Una cadena _delimitador_ puede tener más de un carácter de longitud e incluir caracteres con múltiples bytes.</span><span class="sxs-lookup"><span data-stu-id="4687c-126">A  _delimiter_ string can be more than one character in length and include multibyte characters.</span></span> <span data-ttu-id="4687c-127">El valor predeterminado es un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="4687c-127">The default is a semicolon.</span></span>  <br/> |
| <span data-ttu-id="4687c-128">_valorDeError_</span><span class="sxs-lookup"><span data-stu-id="4687c-128">_errorvalue_</span></span> <br/> |<span data-ttu-id="4687c-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="4687c-129">Optional</span></span>  <br/> |<span data-ttu-id="4687c-130">**Número**</span><span class="sxs-lookup"><span data-stu-id="4687c-130">**Number**</span></span> <br/> | <span data-ttu-id="4687c-p104">Valor especificado por el usuario que debe devolverse en el caso de que el índice no esté incluido en el intervalo. El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="4687c-p104">A user-specified value to return if the index is out of range. The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4687c-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4687c-133">Remarks</span></span>

<span data-ttu-id="4687c-p105">Si la lista comienza o termina con un delimitador, se supone que existe una cadena nula antes o después de la misma. Dos delimitadores consecutivos indican que hay una cadena nula entre ellos.</span><span class="sxs-lookup"><span data-stu-id="4687c-p105">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="4687c-136">Si el índice está fuera del intervalo, Visio devuelve una cadena vacía o el símbolo (token) opcional que el argumento *valorDeError* .</span><span class="sxs-lookup"><span data-stu-id="4687c-136">If the index is out of range, Visio returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="4687c-137">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="4687c-137">Example 1</span></span>

<span data-ttu-id="4687c-138">INDEX(3;"gato;rata;;cabra")</span><span class="sxs-lookup"><span data-stu-id="4687c-138">INDEX(3,"cat;rat;;goat")</span></span>
  
<span data-ttu-id="4687c-139">Devuelve "cabra".</span><span class="sxs-lookup"><span data-stu-id="4687c-139">Returns "goat".</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4687c-140">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="4687c-140">Example 2</span></span>

<span data-ttu-id="4687c-141">INDEX(54,";1;2;3;",,"ERROR")</span><span class="sxs-lookup"><span data-stu-id="4687c-141">INDEX(54,";1;2;3;",,"ERROR")</span></span>
  
<span data-ttu-id="4687c-142">Devuelve "ERROR".</span><span class="sxs-lookup"><span data-stu-id="4687c-142">Returns "ERROR".</span></span>
  

