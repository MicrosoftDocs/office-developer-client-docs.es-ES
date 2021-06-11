---
title: Registrar servicios y proveedores de servicios en MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Last modified: July 18, 2013'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328374"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>Registrar servicios y proveedores de servicios en MapiSvc.inf

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La instalación de un nuevo proveedor en un sistema requiere actualizar el archivo MapiSvc.inf para que apunte al nuevo proveedor. Las propiedades estándar establecidas durante la configuración, que incluyen lo siguiente, informan a MAPI dónde encontrar la biblioteca de vínculos dinámicos del proveedor (.dll):
  
- El **PR_SERVICE_DLL_NAME** se especifica en la **sección [Servicio de** mensajes]. 
    
- El **PR_PROVIDER_DLL_NAME** se especifica en la **sección [Proveedor de** servicios]. 
    
> [!NOTE]
> La expectativa es que establezca el nombre de la cuenta .dll proveedor (sin el sufijo "32"). A continuación, MAPI carga el proveedor buscándolo en la ruta de acceso. 
  
## <a name="putting-a-path-in-mapisvcinf"></a>Poner una ruta de acceso en MapiSvc.inf

La mayoría de las aplicaciones se instalan en Archivos de programa, lo que requiere una actualización de la variable de ruta de acceso para permitir que los proveedores MAPI funcionen. Con algunas restricciones Microsoft Outlook 2010 y Outlook 2013 pueden dar cabida a rutas de acceso completas a proveedores MAPI.
  
Al registrar el proveedor en MapiSvc.inf, puede colocar la ruta  de acceso completa al proveedor en las propiedades MAPI PR_SERVICE_DLL_NAME y **PR_PROVIDER_DLL_NAME**.
  
En cualquiera de las propiedades, la ruta de acceso completa debe estar sin el sufijo "32", ya que MAPI sigue anexando al nombre de archivo antes de buscar el archivo. Esto significa que si registra la ruta de acceso "c:\mypath\myprovider.dll", MAPI intentará cargar "c:\mypath\myprovider32.dll".
  
Dado que mapi de Outlook no se diseñó originalmente para dar cabida a rutas de acceso completas, logra esta inserción del sufijo "32" buscando el primer período en la cadena, lo que significa que las rutas de acceso que contienen otros períodos no pueden funcionar, por lo que no se pueden usar rutas de acceso como "c:\my.path\myprovider.dll" o "c:\mypath\my.provider.dll".
  
En ocasiones, en un proveedor de almacén se generarán identificadores de entrada mediante la **función WrapStoreEntryID,** que toma como parámetro el nombre del proveedor. 
  
> [!IMPORTANT]
> Si usa rutas de acceso completas en MapiSvc.inf, debe usar la misma ruta de acceso en cualquier llamada a **WrapStoreEntryID**. 
  
Además, la ruta de acceso que use se puede convertir a y desde Unicode mediante la página de códigos proporcionada por la [función GetACP.](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) 
  
> [!CAUTION]
> Experimentará un error si elige una ruta de acceso que contenga caracteres que no puedan sobrevivir a un recorrido de ida y vuelta a través de las funciones [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) y [WideCharToMultiByte.](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) 
  
Para una demostración de esta funcionalidad, se ha revisado el ejemplo [de PST](https://github.com/stephenegriffin/Outlook2010CodeSamples) ajustado en GitHub: la funcionalidad pertinente se encuentra en **MergeWithMapiSvc** y **GenerateProviderPath**.
  

