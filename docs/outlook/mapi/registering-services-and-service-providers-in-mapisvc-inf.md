---
title: Registrar servicios y proveedores de servicios en MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Última modificación: 18 de julio de 2013'
ms.openlocfilehash: edb67fde04a3aa27713c3de47a9a0e7f01eb4b97
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399559"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>Registrar servicios y proveedores de servicios en MapiSvc.inf

 
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Instalación de un nuevo proveedor en un sistema requiere la actualización del archivo MapiSvc.inf para que apunte al nuevo proveedor. Las propiedades estándar establecer durante la configuración, que se incluyen los siguientes, informar a MAPI dónde encontrar la biblioteca de vínculos dinámicos (.dll) de un proveedor:
  
- El **PR_SERVICE_DLL_NAME** se especifica en la sección **[Servicio de mensajes]** . 
    
- El **PR_PROVIDER_DLL_NAME** se especifica en la sección **[Servicio proveedor]** . 
    
> [!NOTE]
> La expectativa es establecer el nombre de .dll su proveedor (sin el sufijo "32"). MAPI, a continuación, carga el proveedor busca en la ruta de acceso. 
  
## <a name="putting-a-path-in-mapisvcinf"></a>Colocando una ruta de acceso en MapiSvc.inf

Instalarán la mayoría de las aplicaciones en archivos de programa, que requieren una actualización a la variable de ruta de acceso para permitir que los proveedores de MAPI para que funcione. Con unas cuantas restricciones Microsoft Outlook 2010 y Outlook 2013 pueden dar cabida a rutas de acceso completas a proveedores de MAPI.
  
Al registrar el proveedor en MapiSvc.inf, podría colocar la ruta de acceso completa para el proveedor en las propiedades MAPI **PR_SERVICE_DLL_NAME** y **PR_PROVIDER_DLL_NAME**.
  
En cualquiera de estas propiedades, debe ser la ruta de acceso completa sin el sufijo "32", debido a que continúa MAPI anexar al nombre del archivo antes de buscar el archivo. Esto significa que si se registra la ruta de acceso "c:\mypath\myprovider.dll", MAPI intentará cargar "c:\mypath\myprovider32.dll".
  
Debido a que Outlook MAPI no se diseñó originalmente para dar cabida a rutas de acceso completas, lleva a cabo esta inserción del sufijo "32" buscando el primer período en la cadena, lo que significa que no funcionan las rutas de acceso que contienen otros períodos, por lo que no puede usar como rutas de acceso "c:\my.path\myprovider.dll" o "c:\mypath\my.provider.dll".
  
A veces en un proveedor de almacén generará mediante la función **WrapStoreEntryID** , que toma como parámetro el nombre del proveedor de los identificadores de entrada. 
  
> [!IMPORTANT]
> Si está utilizando rutas de acceso completas en MapiSvc.inf, debe usar la misma ruta de acceso en todas las llamadas a **WrapStoreEntryID**. 
  
Además, la ruta de acceso que se utiliza es posible que se va a convertir a y desde Unicode mediante la página de código proporcionada por la función [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) . 
  
> [!CAUTION]
> Si elige una ruta de acceso que contiene caracteres que no se pueden sobrevivir fácilmente a través de las funciones de [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) y [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) experimentará errores. 
  
Para una demostración de esta funcionalidad, se ha revisado el [ejemplo PST ajustado](https://ol2010mapisamples.codeplex.com/) en CodePlex - la funcionalidad pertinente se encuentra en **MergeWithMapiSvc** y **GenerateProviderPath**.
  

