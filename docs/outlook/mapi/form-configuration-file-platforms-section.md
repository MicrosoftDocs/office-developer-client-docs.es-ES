---
title: Sección Archivo de configuración de formulario [Plataformas]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419131"
---
# <a name="form-configuration-file-platforms-section"></a>Sección Archivo de configuración de formulario [Plataformas]

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La **sección [Plataformas]** enumera el conjunto completo de plataformas admitidas por este formulario. Cada entrada de plataforma consta del prefijo **Platform.** _,_ donde  _string_ es un código de cadena arbitrario para la plataforma. Cada cadena corresponde a la entrada **de CPU** de una sección individual **de [Plataformas].** Cada entrada de una **sección [Plataformas]** define una  _cadena de plataforma_ que hace referencia a una **[Plataforma] posterior.** _cadena de plataforma_ **]** como se muestra aquí. 
  
La **sección [Plataformas]** enumera el conjunto completo de plataformas admitidas por este formulario. Cada entrada de plataforma consta del prefijo **Platform.** _,_ donde  _string_ es un código de cadena arbitrario para la plataforma. Cada cadena corresponde a la entrada **de CPU** de una sección individual **de [Plataformas].** Cada entrada de una **sección [Plataformas]** define una  _cadena de plataforma_ que hace referencia a una **[Plataforma] posterior.** _cadena de plataforma_ **]** como se muestra aquí. 
  
**[Plataformas]**
  
**Plataforma**. _string_  =   _cadena de plataforma_
  
A continuación se muestra un ejemplo de **una sección [Plataformas].** 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

Cada **[Plataforma.** _cadena de plataforma_ **]** contiene las dos entradas necesarias, **CPU** y **OSVersion**. La **entrada** de CPU especifica el procesador y la **entrada OSVersion** especifica el sistema operativo. En **la tabla** siguiente se describen los valores de CPU válidos. 
  
|**Entrada de CPU**|**Procesador**|
|:-----|:-----|
|Ix86  <br/> |Procesadores de la serie Intel 80x86 y Pentium, así como procesadores equivalentes de AMD, Cy gpu, NextGen y otros fabricantes.  <br/> |
|MIPS  <br/> |Procesadores de la serie MIPS R4000.  <br/> |
|AXP  <br/> |Procesador Digital Equipment Corporation Alpha AXP.  <br/> |
|PPC  <br/> |Procesadores de la serie Power PC de Pentium.  <br/> |
|M68  <br/> |Procesadores de la serie de 68 x 00.  <br/> |
   
Los **valores válidos de OSVersion** se describen en la tabla siguiente. 
  
|**Entrada de OSVersion**|**Sistema operativo**|
|:-----|:-----|
|Win3.1  <br/> |Windows 3.1 y Windows para grupos de trabajo 3.11.  <br/> |
|WinNT3.5  <br/> |Windows NT 3.5 o inferior.  <br/> |
|Win95  <br/> |Windows 95.  <br/> |
|WinNT4.0  <br/> |Windows NT 4.0.  <br/> |
|Mac7  <br/> |Sistema Macintosh 7.  <br/> |
   
Además, la **[Plataforma.** _la sección de cadena_ de plataforma **]** debe contener una **entrada File** **o LinkTo.** La **entrada Archivo** muestra el archivo ejecutable de la aplicación del servidor de formularios que la biblioteca de formularios mantiene y carga en un nuevo subdirectorio de la memoria caché de disco cuando se inicia el formulario. Si se **usa una entrada LinkTo** en su lugar, contiene el nombre de una cadena de plataforma diferente de la que se toma la **información** de archivo. Esto resulta útil si una versión de un formulario admite varias plataformas. 
  
La **entrada** del Registro  se usa siempre que se usa la entrada Archivo, identifica la clave del Registro de la biblioteca de formularios donde se almacena el archivo ejecutable de la aplicación del servidor de formularios. Las cadenas precedidas por una barra diagonal inversa ( \ ) se colocan en la raíz del Registro. Las cadenas no precedidas por una barra diagonal inversa se colocan en la HKEY_CLASSES_ROOT\CLSID\  _GUID_\ clave del Registro, donde  _GUID_ es el **GUID** del formulario. Los caracteres "%d" se pueden usar para indicar el nombre de la ruta de acceso del directorio desde el que se ha leído el archivo de configuración del formulario. Esto resulta útil para especificar otros archivos con nombres de ruta de acceso relativos al archivo de configuración del formulario. **Se pueden** especificar varias **entradas** de archivo o registro usando File o Registry como prefijo seguido de cualquier otro texto. Formato de **[Platform.** _cadena de plataforma_ **]** la sección es: 
  
- **[Plataforma.** _cadena de plataforma_ **]**
    
- **CPU**  =   _string_
    
- **OSVersion**  =   _string_
    
- **Archivo**  =   _ruta de acceso_
    
- **LinkTo**  =   _string_
    
- **Registro**  =   _string_
  
A continuación se muestra dos ejemplos **de [Platform.** _platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry. 
  
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

La **[Plataforma.**  la sección de cadena de plataforma **]** se omite al agregar un formulario a la biblioteca de formularios local, cuando se supone que el instalador ha colocado los archivos que convierten el controlador de clase de mensaje en almacenamiento local disponible como se indica en la sección del controlador en el Registro OLE y ha realizado el registro OLE en el registro del sistema. 
  

