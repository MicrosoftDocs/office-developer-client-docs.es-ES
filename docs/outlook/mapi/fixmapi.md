---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383817"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Realiza una copia de seguridad de la copia actual de mapi32.dll en el cliente de equipo y restaura mapi32.dll con la biblioteca de código auxiliar MAPI, mapistub.dll.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportada por:  <br/> |MAPISTUB.dll  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Valores devueltos

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.
  
Si se produce un error en la función, el valor devuelto es cero. Para obtener información de error extendida, llame a la función del Kit de desarrollo de Software (SDK) de Microsoft Windows, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**. 
  
## <a name="remarks"></a>Comentarios

 **FixMAPI** no reemplazar el archivo mapi32.dll actual si el archivo está marcado como de sólo lectura. 
  
 **FixMAPI** no reemplazar el archivo mapi32.dll actual si Microsoft Exchange Server está instalado en el equipo. 
  
Cuando **FixMAPI** realiza una copia de seguridad de la copia actual de mapi32.dll en el equipo, asigna a la copia un nombre distinto de "mapi32.dll". A continuación, dirige las llamadas subsiguientes destinadas a ese ensamblado a la copia de seguridad. 
  
## <a name="see-also"></a>Vea también



[KB 256946: Recibe un mensaje de error de conflicto de programa al iniciar Outlook 2000](https://support.microsoft.com/kb/256946)
  
[KB 228457: Descripción de la herramienta Fixmapi.exe incluidos con Internet Explorer 5](https://support.microsoft.com/kb/228457)

