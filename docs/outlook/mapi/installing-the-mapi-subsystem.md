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
ms.openlocfilehash: c2e135fc031dd3faf5a4e08c50147dfcf7787b5e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817824"
---
# <a name="installing-the-mapi-subsystem"></a>Instalar el subsistema MAPI

  
  
**Hace referencia a**: Outlook 
  
Versiones compatibles de Windows instalan la biblioteca de código auxiliar MAPI, Mapi32.dll, en la _ \<unidad\>_ carpeta \Windows\System32. 
  
Las versiones compatibles de Windows son los siguientes:
  
- Windows 7.
    
- Windows Vista.
    
- Windows Server 2008.
    
- Windows Server 2003.
    
- Windows XP.
    
Para instalar correctamente el subsistema MAPI, instale una aplicación que contiene un subsistema basado en MAPI, como Microsoft Outlook.
  
Puede encontrar información acerca de la instalación de subsistema MAPI de un equipo en el registro del sistema. Todos los valores de las entradas del registro son cadenas de caracteres. 
  
Programas de instalación del servicio de mensajes están responsables de crear la información de instalación en la siguiente clave del registro del sistema: 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
Servicios de mensajes deben agregar entradas al registro del sistema. 
  
La tabla siguiente resume cómo los clientes de recuperar información de la versión para el subsistema MAPI en su equipo.
  
|**Para comprobar**|**Registry**|
|:-----|:-----|
|Disponibilidad de MAPI  <br/> |Busque `MAPIX=1`.  <br/> |
|Versión disponible de MAPI  <br/> |Busca una cadena MAPIXVER del formulario " _x.x.x_".  <br/> |
   
## <a name="see-also"></a>Vea también



[Informaci�n general sobre programaci�n de MAPI](mapi-programming-overview.md)

