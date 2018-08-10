---
title: OPENFILE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: Se abre un documento de Microsoft Visio, si no está abierto y activa la ventana de documento.
ms.openlocfilehash: 7d4778fc4641465e88303b8515365172fd8be0ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822696"
---
# <a name="openfile-function"></a><span data-ttu-id="7591f-103">Función OPENFILE</span><span class="sxs-lookup"><span data-stu-id="7591f-103">OPENFILE Function</span></span>

<span data-ttu-id="7591f-104">Se abre un documento de Microsoft Visio, si no está abierto y activa la ventana de documento.</span><span class="sxs-lookup"><span data-stu-id="7591f-104">Opens a Microsoft Visio document, if it's not already open, and activates the document window.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7591f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7591f-105">Syntax</span></span>

 <span data-ttu-id="7591f-106">**OPENFILE** ( _"nombre de archivo"_)</span><span class="sxs-lookup"><span data-stu-id="7591f-106">**OPENFILE**( _"filename"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="7591f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7591f-107">Parameters</span></span>

|<span data-ttu-id="7591f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="7591f-108">**Name**</span></span>|<span data-ttu-id="7591f-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="7591f-109">**Required/Optional**</span></span>|<span data-ttu-id="7591f-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="7591f-110">**Data Type**</span></span>|<span data-ttu-id="7591f-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7591f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7591f-112">_nombre de archivo_</span><span class="sxs-lookup"><span data-stu-id="7591f-112">_filename_</span></span> <br/> |<span data-ttu-id="7591f-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7591f-113">Required</span></span>  <br/> |<span data-ttu-id="7591f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="7591f-114">**String**</span></span> <br/> |<span data-ttu-id="7591f-115">El nombre del archivo, incluida la ruta de acceso del archivo que desea abrir.</span><span class="sxs-lookup"><span data-stu-id="7591f-115">The name of the file, including file path, you want to open.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7591f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7591f-116">Remarks</span></span>

<span data-ttu-id="7591f-p101">Si hay varias llamadas a la función OPENFILE, se van agregando a una cola y se ejecutan en el orden en que se hayan ido evaluando. Si el documento actual de Visio está activado para modificarlo visualmente, se iniciará una copia nueva de Visio con el nombre de archivo solicitado.</span><span class="sxs-lookup"><span data-stu-id="7591f-p101">Multiple OPENFILE function calls are queued and executed in order of evaluation. If the current Visio document is activated for visual (in-place) editing, a new Visio instance is launched with the requested file name.</span></span> 
  
<span data-ttu-id="7591f-119">Esta función siempre devuelve el valor FALSE.</span><span class="sxs-lookup"><span data-stu-id="7591f-119">This function always returns FALSE.</span></span> 
  
<span data-ttu-id="7591f-p102">En versiones anteriores de la aplicación Visio, esta función se denominaba _OPENFILE. La versión 4.0 de Visio y posteriores aceptan cualquiera de las dos denominaciones.</span><span class="sxs-lookup"><span data-stu-id="7591f-p102">In earlier versions of the Visio application, this function appears as _OPENFILE. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="7591f-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7591f-122">Example</span></span>

 `OPENFILE("C:/MyFile.vsdx")`
  
<span data-ttu-id="7591f-123">Se abre el archivo especificado "MyFile.vsdx" en una ventana nueva o activa la ventana si el archivo ya está abierto.</span><span class="sxs-lookup"><span data-stu-id="7591f-123">Opens the specified file "MyFile.vsdx" in a new window, or activates the window if the file is already open.</span></span> 
  
