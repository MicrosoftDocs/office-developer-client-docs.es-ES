---
title: Instalar el subsistema MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: adb4d09ccce95683ac46e7b271fafa328b1a9f97
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575353"
---
# <a name="installing-the-mapi-subsystem"></a><span data-ttu-id="d7986-103">Instalar el subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="d7986-103">Installing the MAPI Subsystem</span></span>

  
  
<span data-ttu-id="d7986-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7986-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7986-105">Versiones compatibles de Windows instalan la biblioteca de código auxiliar MAPI, Mapi32.dll, en la _ \<unidad\>_ carpeta \Windows\System32.</span><span class="sxs-lookup"><span data-stu-id="d7986-105">Supported versions of Windows install the MAPI stub library, Mapi32.dll, in the  _\<drive\>_ \Windows\System32 folder.</span></span> 
  
<span data-ttu-id="d7986-106">Las versiones compatibles de Windows son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d7986-106">The supported versions of Windows are as follows:</span></span>
  
- <span data-ttu-id="d7986-107">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d7986-107">Windows 7.</span></span>
    
- <span data-ttu-id="d7986-108">Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d7986-108">Windows Vista.</span></span>
    
- <span data-ttu-id="d7986-109">Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d7986-109">Windows Server 2008.</span></span>
    
- <span data-ttu-id="d7986-110">Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d7986-110">Windows Server 2003.</span></span>
    
- <span data-ttu-id="d7986-111">Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d7986-111">Windows XP.</span></span>
    
<span data-ttu-id="d7986-112">Para instalar correctamente el subsistema MAPI, instale una aplicación que contiene un subsistema basado en MAPI, como Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="d7986-112">To correctly install the MAPI subsystem, install an application that contains a MAPI-based subsystem, such as Microsoft Outlook.</span></span>
  
<span data-ttu-id="d7986-113">Puede encontrar información acerca de la instalación de subsistema MAPI de un equipo en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="d7986-113">You can find information about a computer's MAPI subsystem installation in the system registry.</span></span> <span data-ttu-id="d7986-114">Todos los valores de las entradas del registro son cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d7986-114">All values in the registry entries are character strings.</span></span> 
  
<span data-ttu-id="d7986-115">Programas de instalación del servicio de mensajes están responsables de crear la información de instalación en la siguiente clave del registro del sistema:</span><span class="sxs-lookup"><span data-stu-id="d7986-115">Message service installation programs are responsible for creating the installation information in the following system registry key:</span></span> 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
<span data-ttu-id="d7986-116">Servicios de mensajes deben agregar entradas al registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="d7986-116">Message services must add entries to the system registry.</span></span> 
  
<span data-ttu-id="d7986-117">La tabla siguiente resume cómo los clientes de recuperar información de la versión para el subsistema MAPI en su equipo.</span><span class="sxs-lookup"><span data-stu-id="d7986-117">The following table summarizes how clients retrieve version information for the MAPI subsystem on their computer.</span></span>
  
|<span data-ttu-id="d7986-118">**Para comprobar**</span><span class="sxs-lookup"><span data-stu-id="d7986-118">**To check**</span></span>|<span data-ttu-id="d7986-119">**Registry**</span><span class="sxs-lookup"><span data-stu-id="d7986-119">**Registry**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d7986-120">Disponibilidad de MAPI</span><span class="sxs-lookup"><span data-stu-id="d7986-120">Availability of MAPI</span></span>  <br/> |<span data-ttu-id="d7986-121">Busque `MAPIX=1`.</span><span class="sxs-lookup"><span data-stu-id="d7986-121">Look for  `MAPIX=1`.</span></span>  <br/> |
|<span data-ttu-id="d7986-122">Versión disponible de MAPI</span><span class="sxs-lookup"><span data-stu-id="d7986-122">Available version of MAPI</span></span>  <br/> |<span data-ttu-id="d7986-123">Busca una cadena MAPIXVER del formulario " _x.x.x_".</span><span class="sxs-lookup"><span data-stu-id="d7986-123">Look for a MAPIXVER string of the form " _x.x.x_".</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7986-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d7986-124">See also</span></span>



[<span data-ttu-id="d7986-125">Informaci�n general sobre programaci�n de MAPI</span><span class="sxs-lookup"><span data-stu-id="d7986-125">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

