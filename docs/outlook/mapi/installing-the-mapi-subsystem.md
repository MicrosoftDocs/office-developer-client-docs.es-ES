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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309642"
---
# <a name="installing-the-mapi-subsystem"></a>Instalar el subsistema MAPI

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Las versiones compatibles de Windows instalan la biblioteca de códigos auxiliares de MAPI, Mapi32.dll, en la carpeta \Windows\System32 de la _\<unidad\>_. 
  
Las versiones compatibles de Windows son los siguientes:
  
- Windows 7.
    
- Windows Vista.
    
- Windows Server 2008.
    
- Windows Server 2003.
    
- Windows XP.
    
Para instalar correctamente el subsistema MAPI, instale una aplicación que contenga un subsistema basado en MAPI, como por ejemplo Microsoft Outlook.
  
Puede encontrar información sobre la instalación de subsistema MAPI del equipo en el registro del sistema. Todos los valores de las entradas del registro son cadenas de caracteres. 
  
Los programas de instalación del servicio de mensajes son responsables de crear la información de instalación en la siguiente clave del registro del sistema: 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
Los servicios de mensajes deben agregar entradas al registro del sistema. 
  
La siguiente tabla resume cómo los clientes recuperan información de versiones para el subsistema MAPI en su equipo.
  
|**Comprobar**|**Registro**|
|:-----|:-----|
|Disponibilidad de MAPI  <br/> |Buscar  `MAPIX=1`.  <br/> |
|Versión disponible de MAPI  <br/> |Buscar una cadena MAPIXVER del formulario " _x.x.x_".  <br/> |
   
## <a name="see-also"></a>Vea también



[Información general sobre programación de MAPI](mapi-programming-overview.md)

