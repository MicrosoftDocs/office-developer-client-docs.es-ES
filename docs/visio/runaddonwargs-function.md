---
title: RUNADDONWARGS (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251493
localization_priority: Normal
ms.assetid: c154413f-c366-a66b-94e3-ed71ad23f325
description: Ejecuta la cadena y pasa los argumentos de la línea de comandos al programa como una cadena.
ms.openlocfilehash: bc05a4480438875c348373059f57bf04f82c9eca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318952"
---
# <a name="runaddonwargs-function"></a><span data-ttu-id="e8d8b-103">Función RUNADDONWARGS</span><span class="sxs-lookup"><span data-stu-id="e8d8b-103">RUNADDONWARGS Function</span></span>

<span data-ttu-id="e8d8b-104">Ejecuta la _cadena_ y pasa los _argumentos_ de la línea de comandos al programa como una cadena.</span><span class="sxs-lookup"><span data-stu-id="e8d8b-104">Runs  _string_ and passes the command line  _arguments_ to the program as a string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e8d8b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8d8b-105">Syntax</span></span>

<span data-ttu-id="e8d8b-106">RUNADDONWARGS ("\* \* *cadena* \* *", "* \* *argumentos* \* \*")</span><span class="sxs-lookup"><span data-stu-id="e8d8b-106">RUNADDONWARGS(" \*\* *string* \*\* "," \*\* *arguments* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e8d8b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8d8b-107">Parameters</span></span>

|<span data-ttu-id="e8d8b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e8d8b-108">**Name**</span></span>|<span data-ttu-id="e8d8b-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e8d8b-109">**Required/Optional**</span></span>|<span data-ttu-id="e8d8b-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="e8d8b-110">**Data Type**</span></span>|<span data-ttu-id="e8d8b-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8d8b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e8d8b-112">_string_</span><span class="sxs-lookup"><span data-stu-id="e8d8b-112">_string_</span></span> <br/> |<span data-ttu-id="e8d8b-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e8d8b-113">Required</span></span>  <br/> |<span data-ttu-id="e8d8b-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e8d8b-114">**String**</span></span> <br/> | <span data-ttu-id="e8d8b-115">Nombre de un complemento.</span><span class="sxs-lookup"><span data-stu-id="e8d8b-115">The name of an add-on.</span></span>  <br/> |
| <span data-ttu-id="e8d8b-116">_argumentos_</span><span class="sxs-lookup"><span data-stu-id="e8d8b-116">_arguments_</span></span> <br/> |<span data-ttu-id="e8d8b-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e8d8b-117">Required</span></span>  <br/> |<span data-ttu-id="e8d8b-118">**String**</span><span class="sxs-lookup"><span data-stu-id="e8d8b-118">**String**</span></span> <br/> |<span data-ttu-id="e8d8b-119">Argumentos por pasar al programa.</span><span class="sxs-lookup"><span data-stu-id="e8d8b-119">Arguments to pass to your program.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8d8b-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8d8b-120">Remarks</span></span>

<span data-ttu-id="e8d8b-121">En la práctica, los _argumentos_ deben ser de 50 o menos caracteres.</span><span class="sxs-lookup"><span data-stu-id="e8d8b-121">In practice,  _arguments_ should be 50 or fewer characters.</span></span> <span data-ttu-id="e8d8b-122">Utilice la función RUNADDONWARGS para enlazar un programa, por ejemplo un complemento, a una celda (por ejemplo, a una celda Action o Events).</span><span class="sxs-lookup"><span data-stu-id="e8d8b-122">Use the RUNADDONWARGS function to bind a program, such as an add-on, to a cell, for example, to an Action or Events cell.</span></span> 
  
<span data-ttu-id="e8d8b-123">La función RUNADDONWARGS sólo puede ejecutar complementos que son miembros de la colección Addons \*\*\*\* de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e8d8b-123">The RUNADDONWARGS function can only run add-ons that are members of the application's **Addons** collection.</span></span> <span data-ttu-id="e8d8b-124">Para estar presente en esa colección, un complemento debe ser un archivo EXE o un archivo VSL que:</span><span class="sxs-lookup"><span data-stu-id="e8d8b-124">To be present in that collection, an add-on must be an EXE file or VSL file that is:</span></span> 
  
- <span data-ttu-id="e8d8b-125">Instalado en la ruta **Startup** o **Addons** de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e8d8b-125">Installed in the application's **Startup** or **Addons** path.</span></span> 
    
- <span data-ttu-id="e8d8b-126">Programado mediante el método **Add** de la colección **Addons**.</span><span class="sxs-lookup"><span data-stu-id="e8d8b-126">Added programmatically by using the **Add** method of the **Addons** collection.</span></span> 
    
<span data-ttu-id="e8d8b-127">Para obtener más información acerca de cómo ejecutar código en Visio, vea [Acerca de la configuración de seguridad y la ejecución de código en Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) en esta Referencia de ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="e8d8b-127">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="e8d8b-p103">En versiones anteriores de Visio, esta función se denominaba _RUNADDONWARGS. La versión 4.0 de Visio y las posteriores aceptan cualquiera de las dos denominaciones.</span><span class="sxs-lookup"><span data-stu-id="e8d8b-p103">In earlier versions of Visio, this function appears as _RUNADDONWARGS. Visio application versions 4.0 and later accept either style.</span></span>
  
## <a name="example"></a><span data-ttu-id="e8d8b-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8d8b-130">Example</span></span>

<span data-ttu-id="e8d8b-131">RUNADDONWARGS ("GRAPHMKR. EXE ","/GraphMaker = stack ")</span><span class="sxs-lookup"><span data-stu-id="e8d8b-131">RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack")</span></span> 
  
<span data-ttu-id="e8d8b-132">Inicia el complemento Graphmkr.exe y le pasa el argumento /GraphMaker=Stack.</span><span class="sxs-lookup"><span data-stu-id="e8d8b-132">Launches the add-on Graphmkr.exe and passes it the argument /GraphMaker=Stack.</span></span> 
  

