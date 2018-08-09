---
title: NAME (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251580
localization_priority: Normal
ms.assetid: 1ca67a09-9df2-37f5-b269-e761d76bb011
description: Devuelve el nombre de una hoja como una cadena.
ms.openlocfilehash: 0d3a70573177d8e16a16972d0a08245381b209dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822668"
---
# <a name="name-function"></a><span data-ttu-id="f8939-103">Función NAME</span><span class="sxs-lookup"><span data-stu-id="f8939-103">NAME Function</span></span>

<span data-ttu-id="f8939-104">Devuelve el nombre de una hoja como una cadena.</span><span class="sxs-lookup"><span data-stu-id="f8939-104">Returns a sheet's name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f8939-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8939-105">Syntax</span></span>

<span data-ttu-id="f8939-106">NOMBRE (** *IdIdiomaOpc* **)</span><span class="sxs-lookup"><span data-stu-id="f8939-106">NAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f8939-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8939-107">Parameters</span></span>

|<span data-ttu-id="f8939-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f8939-108">**Name**</span></span>|<span data-ttu-id="f8939-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="f8939-109">**Required/Optional**</span></span>|<span data-ttu-id="f8939-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="f8939-110">**Data Type**</span></span>|<span data-ttu-id="f8939-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f8939-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f8939-112">_IdIdiomaOpc_</span><span class="sxs-lookup"><span data-stu-id="f8939-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="f8939-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="f8939-113">Optional</span></span>  <br/> |<span data-ttu-id="f8939-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="f8939-114">**Number**</span></span> <br/> |<span data-ttu-id="f8939-p101">Se usa para especificar un idioma para la cadena devuelta por la función. Use 0 (valor predeterminado) para especificar el idioma local. Use 750 para especificar un idioma universal.</span><span class="sxs-lookup"><span data-stu-id="f8939-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f8939-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8939-118">Return value</span></span>

<span data-ttu-id="f8939-119">String</span><span class="sxs-lookup"><span data-stu-id="f8939-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f8939-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8939-120">Remarks</span></span>

<span data-ttu-id="f8939-121">Si el código de idioma indicado no es válido, se utiliza el idioma local.</span><span class="sxs-lookup"><span data-stu-id="f8939-121">If you pass an illegal language code, the local language is used.</span></span> 
  

