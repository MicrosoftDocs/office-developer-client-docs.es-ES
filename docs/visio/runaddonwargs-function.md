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
description: Ejecuta cadena y le pasa los argumentos de línea de comandos para el programa como una cadena.
ms.openlocfilehash: 7bc05a0cbf32550d1e39bee39bec83101882cf19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823093"
---
# <a name="runaddonwargs-function"></a><span data-ttu-id="3afb0-103">Función RUNADDONWARGS</span><span class="sxs-lookup"><span data-stu-id="3afb0-103">RUNADDONWARGS Function</span></span>

<span data-ttu-id="3afb0-104">Ejecuta _cadena_ y le pasa los _argumentos_ de línea de comandos para el programa como una cadena.</span><span class="sxs-lookup"><span data-stu-id="3afb0-104">Runs  _string_ and passes the command line  _arguments_ to the program as a string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3afb0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3afb0-105">Syntax</span></span>

<span data-ttu-id="3afb0-106">RUNADDONWARGS ("** *cadena* **","** *argumentos* **")</span><span class="sxs-lookup"><span data-stu-id="3afb0-106">RUNADDONWARGS(" ** *string* ** "," ** *arguments* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3afb0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3afb0-107">Parameters</span></span>

|<span data-ttu-id="3afb0-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="3afb0-108">**Name**</span></span>|<span data-ttu-id="3afb0-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="3afb0-109">**Required/Optional**</span></span>|<span data-ttu-id="3afb0-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="3afb0-110">**Data Type**</span></span>|<span data-ttu-id="3afb0-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3afb0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3afb0-112">_string_</span><span class="sxs-lookup"><span data-stu-id="3afb0-112">_string_</span></span> <br/> |<span data-ttu-id="3afb0-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="3afb0-113">Required</span></span>  <br/> |<span data-ttu-id="3afb0-114">**String**</span><span class="sxs-lookup"><span data-stu-id="3afb0-114">**String**</span></span> <br/> | <span data-ttu-id="3afb0-115">Nombre de un complemento.</span><span class="sxs-lookup"><span data-stu-id="3afb0-115">The name of an add-on.</span></span>  <br/> |
| <span data-ttu-id="3afb0-116">_argumentos_</span><span class="sxs-lookup"><span data-stu-id="3afb0-116">_arguments_</span></span> <br/> |<span data-ttu-id="3afb0-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="3afb0-117">Required</span></span>  <br/> |<span data-ttu-id="3afb0-118">**String**</span><span class="sxs-lookup"><span data-stu-id="3afb0-118">**String**</span></span> <br/> |<span data-ttu-id="3afb0-119">Argumentos por pasar al programa.</span><span class="sxs-lookup"><span data-stu-id="3afb0-119">Arguments to pass to your program.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3afb0-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3afb0-120">Remarks</span></span>

<span data-ttu-id="3afb0-121">En la práctica, _los argumentos_ deben ser 50 o menos caracteres.</span><span class="sxs-lookup"><span data-stu-id="3afb0-121">In practice,  _arguments_ should be 50 or fewer characters.</span></span> <span data-ttu-id="3afb0-122">Utilice la función RUNADDONWARGS para enlazar un programa, como un complemento a una celda, por ejemplo, a una celda Action o Events.</span><span class="sxs-lookup"><span data-stu-id="3afb0-122">Use the RUNADDONWARGS function to bind a program, such as an add-on, to a cell, for example, to an Action or Events cell.</span></span> 
  
<span data-ttu-id="3afb0-p102">La función RUNADDONWARGS sólo puede ejecutar complementos que pertenecen a la colección **Addons** de la aplicación.Para formar parte de ese conjunto, el complemento debe consistir en un archivo EXE o VSL que haya sido:</span><span class="sxs-lookup"><span data-stu-id="3afb0-p102">The RUNADDONWARGS function can only run add-ons that are members of the application's **Addons** collection. To be present in that collection, an add-on must be an EXE file or VSL file that is:</span></span> 
  
- <span data-ttu-id="3afb0-125">Instalado en la ruta **Startup** o **Addons** de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3afb0-125">Installed in the application's **Startup** or **Addons** path.</span></span> 
    
- <span data-ttu-id="3afb0-126">Programado mediante el método **Add** de la colección **Addons**.</span><span class="sxs-lookup"><span data-stu-id="3afb0-126">Added programmatically by using the **Add** method of the **Addons** collection.</span></span> 
    
<span data-ttu-id="3afb0-127">Para obtener más información acerca de cómo ejecutar código en Visio, vea [Acerca de la configuración de seguridad y la ejecución de código en Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) en esta Referencia de ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="3afb0-127">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="3afb0-p103">En versiones anteriores de Visio, esta función se denominaba _RUNADDONWARGS. La versión 4.0 de Visio y las posteriores aceptan cualquiera de las dos denominaciones.</span><span class="sxs-lookup"><span data-stu-id="3afb0-p103">In earlier versions of Visio, this function appears as _RUNADDONWARGS. Visio application versions 4.0 and later accept either style.</span></span>
  
## <a name="example"></a><span data-ttu-id="3afb0-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3afb0-130">Example</span></span>

<span data-ttu-id="3afb0-131">RUNADDONWARGS ("GRAPHMKR. EXE"," / GraphMaker = Stack ")</span><span class="sxs-lookup"><span data-stu-id="3afb0-131">RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack")</span></span> 
  
<span data-ttu-id="3afb0-132">Inicia el complemento Graphmkr.exe y le pasa el argumento /GraphMaker=Stack.</span><span class="sxs-lookup"><span data-stu-id="3afb0-132">Launches the add-on Graphmkr.exe and passes it the argument /GraphMaker=Stack.</span></span> 
  

