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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334964"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Realiza una copia de seguridad de la copia actual de Mapi32. dll en el equipo cliente y restaura Mapi32. dll con la biblioteca de código auxiliar de MAPI, MAPISTUB. dll.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|ExPortado por:  <br/> |MAPISTUB. dll  <br/> |
|Llamado por:  <br/> |Client  <br/> |
|Implementado por:  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Valores devueltos

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.
  
Si se produce un error en la función, el valor devuelto es cero. Para obtener información ampliada del error, llame a la función del kit de desarrollo de software (SDK) de Microsoft Windows, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**. 
  
## <a name="remarks"></a>Comentarios

 **FixMAPI** no reemplaza el archivo Mapi32. dll actual si el archivo está marcado como de solo lectura. 
  
 **FixMAPI** no reemplaza el archivo Mapi32. dll actual si Microsoft Exchange Server está instalado en el equipo. 
  
Cuando **FixMAPI** hace una copia de seguridad de la copia actual de Mapi32. dll en el equipo, asigna a la copia de seguridad un nombre distinto de "Mapi32. dll". A continuación, dirige las llamadas posteriores dirigidas a ese ensamblado a la copia de seguridad. 
  
## <a name="see-also"></a>Vea también



[KB 256946: recibe un mensaje de error de conflicto de programas al iniciar Outlook 2000](https://support.microsoft.com/kb/256946)
  
[KB 228457: Descripción de la herramienta Fixmapi. exe que se incluye con Internet Explorer 5](https://support.microsoft.com/kb/228457)

