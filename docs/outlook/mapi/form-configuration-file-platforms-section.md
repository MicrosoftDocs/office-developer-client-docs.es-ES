---
title: Sección del archivo de configuración de formulario [plataformas]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327513"
---
# <a name="form-configuration-file-platforms-section"></a>Sección del archivo de configuración de formulario [plataformas]

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La sección **[Platforms]** muestra el conjunto completo de plataformas compatibles con este formulario. Cada entrada de la plataforma consta de la plataforma de prefijo **.** _String_, donde _String_ es un código de cadena arbitrario de la plataforma. Cada cadena corresponde a la entrada de la **CPU** de una sección **[Platforms]** individual. Cada entrada de una sección **[Platforms]** define una _cadena de plataforma_ que hace referencia a una siguiente **[plataforma.** _cadena_ de la plataforma **]** tal como se muestra aquí. 
  
La sección **[Platforms]** muestra el conjunto completo de plataformas compatibles con este formulario. Cada entrada de la plataforma consta de la plataforma de prefijo **.** _String_, donde _String_ es un código de cadena arbitrario de la plataforma. Cada cadena corresponde a la entrada de la **CPU** de una sección **[Platforms]** individual. Cada entrada de una sección **[Platforms]** define una _cadena de plataforma_ que hace referencia a una siguiente **[plataforma.** _cadena_ de la plataforma **]** tal como se muestra aquí. 
  
**Select**
  
**Plataforma**. __ =  cadena de_plataforma_ de cadena
  
A continuación se encuentra un ejemplo de una sección **[Platforms]** . 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

Cada **[plataforma.** _cadena_ de la plataforma **]** contiene las dos entradas requeridas, **CPU** y **OSVersion**. La entrada **CPU** especifica el procesador y la entrada **OSVersion** especifica el sistema operativo. Los valores de **CPU** válidos se describen en la tabla siguiente. 
  
|**Entrada de CPU**|**Procesador**|
|:-----|:-----|
|Ix86  <br/> |Procesadores Intel 80x86 y Pentium series, así como procesadores equivalentes de AMD, Cyrix, NextGen y otros fabricantes.  <br/> |
|MIPS  <br/> |Procesadores MIPS de la serie R4000.  <br/> |
|AXP  <br/> |Procesador Digital Equipment Corporation Alpha AXP.  <br/> |
|PPC  <br/> |Procesadores de Motorola Power PC Series.  <br/> |
|M68  <br/> |Mororola procesadores de la serie 68x00.  <br/> |
   
Los valores de **OSVersion** válidos se describen en la tabla siguiente. 
  
|**Entrada OSVersion**|**Sistema operativo**|
|:-----|:-----|
|Win 3.1  <br/> |Windows 3,1 y Windows para trabajo en grupo 3,11.  <br/> |
|Winnt 3.5  <br/> |Windows NT 3,5 o anterior.  <br/> |
|95  <br/> |Windows 95.  <br/> |
|WinNT 4.0  <br/> |Windows NT 4,0.  <br/> |
|Mac7  <br/> |Sistema Macintosh 7.  <br/> |
   
Además, **[plataforma.** _cadena_ de la plataforma **]** debe contener una entrada **File** o **LinkTo** . La entrada **File** muestra el archivo ejecutable de la aplicación de servidor de formulario que mantiene la biblioteca de formularios y se carga en un nuevo subdirectorio de la caché de disco cuando se inicia el formulario. Si se **** usa una entrada LinkTo, ésta contiene el nombre de una cadena de plataforma diferente desde la que se toma la información del **archivo** . Esto es útil si una versión de un formulario admite varias plataformas. 
  
La entrada **del registro** se usa siempre que se utiliza la entrada del **archivo** , identifica la clave del registro de la biblioteca de formularios en la que se almacena el archivo ejecutable de la aplicación de servidor de formularios. Las cadenas precedidas por una barra diagonal inversa (\) se colocan en la raíz del registro. Las cadenas que no estén precedidas por una barra diagonal inversa se colocan en la clave del registro HKEY_CLASSES_ROOT\CLSID\ _GUID_\, donde _GUID_ es el **GUID** del formulario. Se pueden usar los caracteres "% d" para indicar la ruta de la ruta de directorio desde la que se leyó el archivo de configuración del formulario. Esto es útil para especificar otros archivos con rutas de nombres en relación con el archivo de configuración de formulario. Se pueden especificar varias entradas de **archivo** o **registro** mediante archivo o registro como prefijo seguido de cualquier otro texto. El formato de **[plataforma.** _cadena_ de la plataforma **]** es: 
  
- **Varias.** _cadena_ de la plataforma **]**
    
- **** =  _Cadena_ de CPU
    
- **** =  _Cadena_ OSVersion
    
- **** =  _Ruta de acceso_ del archivo
    
- **** =  _Cadena_ LinkTo
    
- **Cadena del registro** =  __
  
A continuación se muestran dos ejemplos **[Platform.** _cadena_ de la plataforma **]** secciones, una con la entrada de **archivo** y otra con **** la entrada LinkTo. 
  
```cpp
[Platform.NTx86]
CPU = ix86
OSVersion = WinNT3.5
File = \helpdesk.exe
Registry = Local Server = %d\helpdesk.exe
[Platform.Win95]
CPU = ix86
OSVersion = Win95
LinkTo = NTx86

```

**[Plataforma.** _cadena_ de la plataforma **]** se omite cuando se agrega un formulario a la biblioteca de formularios local cuando se da por sentado que el instalador ha colocado los archivos que conforman el controlador de clase de mensaje en el almacenamiento local disponible como se indica en la sección del controlador del registro OLE y ha realizado el registro OLE en el registro del sistema. 
  

