---
title: Inicio de una sesión MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d88ce382b6a6b5f98ec5f88c4deb1565d3b60151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336347"
---
# <a name="starting-a-mapi-session"></a>Inicio de una sesión MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Aunque hay una cantidad significativa de trabajo realizado durante el inicio de la sesión, las tareas necesarias son mínimas. Gran parte de este trabajo se realiza en el procesamiento MAPI de las llamadas [MAPIInitialize](mapiinitialize.md) y [MAPILogonEx.](mapilogonex.md) Ambas funciones aceptan marcas como parámetros de entrada para controlar aspectos de la sesión, como el control de notificaciones y la interfaz de usuario. Es importante comprender las consecuencias de establecer cada una de estas marcas al llamar a **MAPIInitialize** para inicializar las bibliotecas MAPI y **MAPILogonEx** para iniciar sesión en el subsistema MAPI. 
  
 **Para iniciar una sesión MAPI**
  
1. Llama **a MAPIInitialize** para inicializar el conjunto estándar de bibliotecas MAPI. 
    
2. Si necesita usar las bibliotecas OLE, llame a la función [OLE OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).
    
3. Si necesita usar la biblioteca de utilidades MAPI, llame [a ScInitMapiUtil](scinitmapiutil.md).
    
4. Llame **a MAPILogonEx** con un perfil válido para iniciar sesión en el subsistema MAPI. **MAPILogonEx comprueba** la configuración de cada uno de los proveedores de servicios en los servicios de mensajes incluidos en el perfil, solicitando al usuario información adicional si es necesario y posible. Cuando **MAPILogonEx** finaliza, los proveedores de servicios configurados están listos para el servicio. 
    
## <a name="in-this-section"></a>En esta sección

[Inicializar MAPI](initializing-mapi.md)
  
> Describe cómo inicializar MAPI para una sesión.
    
[Inicializar OLE para MAPI](initializing-ole-for-mapi.md)
  
> Describe las llamadas que se deben realizar para inicializar OLE para su uso con MAPI.
    
[Inicialización de las utilidades MAPI](initializing-the-mapi-utilities.md)
  
> Describe cómo inicializar las utilidades MAPI.
    
[Iniciar sesión en MAPI](logging-on-to-mapi.md)
  
> Describe cómo las aplicaciones cliente inician sesión en el subs sistema MAPI.
    

