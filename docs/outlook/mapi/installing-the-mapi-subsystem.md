---
title: Instalar el subsistema MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Última modificación: 09 de marzo de 2015'
localization_priority: Priority
ms.openlocfilehash: 112a683f5967f8740c2d21285eb4ebbc0f455c48
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722441"
---
# <a name="installing-the-mapi-subsystem"></a><span data-ttu-id="6a358-103">Instalar el subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="6a358-103">Installing the MAPI Subsystem</span></span>

  
  
<span data-ttu-id="6a358-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a358-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a358-105">Las versiones compatibles de Windows instalan la biblioteca de códigos auxiliares de MAPI, Mapi32.dll, en la carpeta \Windows\System32 de la _\<unidad\>_.</span><span class="sxs-lookup"><span data-stu-id="6a358-105">Supported versions of Windows install the MAPI stub library, Mapi32.dll, in the  _\<drive\>_ \Windows\System32 folder.</span></span> 
  
<span data-ttu-id="6a358-106">Las versiones compatibles de Windows son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="6a358-106">The supported versions of Windows are as follows:</span></span>
  
- <span data-ttu-id="6a358-107">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6a358-107">Windows 7</span></span>
    
- <span data-ttu-id="6a358-108">Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6a358-108">Windows Vista</span></span>
    
- <span data-ttu-id="6a358-109">Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6a358-109">Windows Server 2008</span></span>
    
- <span data-ttu-id="6a358-110">Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6a358-110">Windows Server 2003</span></span>
    
- <span data-ttu-id="6a358-111">Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6a358-111">Windows XP</span></span>
    
<span data-ttu-id="6a358-112">Para instalar correctamente el subsistema MAPI, instale una aplicación que contenga un subsistema basado en MAPI, como por ejemplo Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="6a358-112">To correctly install the MAPI subsystem, install an application that contains a MAPI-based subsystem, such as Microsoft Outlook.</span></span>
  
<span data-ttu-id="6a358-113">Puede encontrar información sobre la instalación de subsistema MAPI del equipo en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="6a358-113">You can find information about a computer's MAPI subsystem installation in the system registry.</span></span> <span data-ttu-id="6a358-114">Todos los valores de las entradas del registro son cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6a358-114">All values in the registry entries are character strings.</span></span> 
  
<span data-ttu-id="6a358-115">Los programas de instalación del servicio de mensajes son responsables de crear la información de instalación en la siguiente clave del registro del sistema:</span><span class="sxs-lookup"><span data-stu-id="6a358-115">Message service installation programs are responsible for creating the installation information in the following system registry key:</span></span> 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
<span data-ttu-id="6a358-116">Los servicios de mensajes deben agregar entradas al registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="6a358-116">Message services must add entries to the system registry.</span></span> 
  
<span data-ttu-id="6a358-117">La siguiente tabla resume cómo los clientes recuperan información de versiones para el subsistema MAPI en su equipo.</span><span class="sxs-lookup"><span data-stu-id="6a358-117">The following table summarizes how clients retrieve version information for the MAPI subsystem on their computer.</span></span>
  
|<span data-ttu-id="6a358-118">**Comprobar**</span><span class="sxs-lookup"><span data-stu-id="6a358-118">**To check**</span></span>|<span data-ttu-id="6a358-119">**Registro**</span><span class="sxs-lookup"><span data-stu-id="6a358-119">**Registry**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6a358-120">Disponibilidad de MAPI</span><span class="sxs-lookup"><span data-stu-id="6a358-120">Availability of MAPI</span></span>  <br/> |<span data-ttu-id="6a358-121">Buscar  `MAPIX=1`.</span><span class="sxs-lookup"><span data-stu-id="6a358-121">Look for  `MAPIX=1`.</span></span>  <br/> |
|<span data-ttu-id="6a358-122">Versión disponible de MAPI</span><span class="sxs-lookup"><span data-stu-id="6a358-122">Available version of MAPI</span></span>  <br/> |<span data-ttu-id="6a358-123">Buscar una cadena MAPIXVER del formulario " _x.x.x_".</span><span class="sxs-lookup"><span data-stu-id="6a358-123">Look for a MAPIXVER string of the form " _x.x.x_".</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a358-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a358-124">See also</span></span>



[<span data-ttu-id="6a358-125">Información general sobre programación de MAPI</span><span class="sxs-lookup"><span data-stu-id="6a358-125">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

