---
title: Volver a configurar un proveedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ec5a431d04799e3f19c23dd0437aeac13fbf0968
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820482"
---
# <a name="reconfiguring-a-transport-provider"></a><span data-ttu-id="f0b69-103">Volver a configurar un proveedor de transporte</span><span class="sxs-lookup"><span data-stu-id="f0b69-103">Reconfiguring a Transport Provider</span></span>

  
  
<span data-ttu-id="f0b69-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f0b69-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f0b69-105">Puede usar el objeto de estado del proveedor de transporte para cambiar algunas de las propiedades del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f0b69-105">You can use a transport provider's status object to change some of the properties of the provider.</span></span> <span data-ttu-id="f0b69-106">El intervalo de las propiedades que se pueden cambiar depende de las propiedades que se incluyen con la hoja de propiedades del proveedor y cómo se definen esas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f0b69-106">The range of properties that can be changed depends on the properties that are included with the provider's property sheet and how those properties are defined.</span></span> 
  
 <span data-ttu-id="f0b69-107">**Para volver a configurar un proveedor de transporte activo**</span><span class="sxs-lookup"><span data-stu-id="f0b69-107">**To reconfigure an active transport provider**</span></span>
  
1. <span data-ttu-id="f0b69-108">Llame a [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="f0b69-108">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="f0b69-109">Busque la fila para el proveedor de transporte volver a configurarse mediante la creación de una restricción de propiedad que coincide con **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) con el nombre del proveedor de destino.</span><span class="sxs-lookup"><span data-stu-id="f0b69-109">Locate the row for the transport provider to be reconfigured by creating a property restriction that matches **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the target provider.</span></span> 
    
3. <span data-ttu-id="f0b69-110">Llamar a [IMAPITable:: FindRow](imapitable-findrow.md) para recuperar la fila apropiada.</span><span class="sxs-lookup"><span data-stu-id="f0b69-110">Call [IMAPITable::FindRow](imapitable-findrow.md) to retrieve the appropriate row.</span></span> 
    
4. <span data-ttu-id="f0b69-111">Compruebe que se han establecido los indicadores STATUS_SETTINGS_DIALOG y STATUS_VALIDATE_STATE en propiedad de **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) del proveedor de transporte de destino.</span><span class="sxs-lookup"><span data-stu-id="f0b69-111">Check that the STATUS_SETTINGS_DIALOG and STATUS_VALIDATE_STATE flags are set in the target transport provider's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span> <span data-ttu-id="f0b69-112">Si STATUS_SETTINGS_DIALOG no está establecido, el proveedor de transporte no se muestra una hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="f0b69-112">If STATUS_SETTINGS_DIALOG is not set, the transport provider does not display a configuration property sheet.</span></span> <span data-ttu-id="f0b69-113">Si no se establece STATUS_VALIDATE_STATE, no se puede realizar la reconfiguración dinámica.</span><span class="sxs-lookup"><span data-stu-id="f0b69-113">If STATUS_VALIDATE_STATE is not set, you cannot perform dynamic reconfiguration.</span></span>
    
5. <span data-ttu-id="f0b69-114">Si se establece STATUS_SETTINGS_DIALOG, llame a [SettingsDialog](imapistatus-settingsdialog.md) para mostrar la hoja de propiedades del proveedor de transporte y permitir que el usuario realizar cambios.</span><span class="sxs-lookup"><span data-stu-id="f0b69-114">If STATUS_SETTINGS_DIALOG is set, call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the transport provider's property sheet and allow the user to make changes.</span></span> 
    
6. <span data-ttu-id="f0b69-115">Después de que el usuario ha terminado con la reconfiguración, llamar a [IMAPIStatus::ValidateState](imapistatus-validatestate.md) si se establece STATUS_VALIDATE_STATE, pasando CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="f0b69-115">After the user has finished with the reconfiguration, call [IMAPIStatus::ValidateState](imapistatus-validatestate.md) if STATUS_VALIDATE_STATE is set, passing CONFIG_CHANGED.</span></span> 
    

