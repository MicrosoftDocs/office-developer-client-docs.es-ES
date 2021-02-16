---
title: Ejemplo de proveedor de libreta de direcciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331111"
---
# <a name="address-book-provider-sample"></a>Ejemplo de proveedor de libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este ejemplo admite un único contenedor de solo lectura para nombres para mostrar y direcciones de correo electrónico, que se leen desde un archivo binario plano. El ejemplo admite plantillas de uso único y todas las opciones de configuración excepto el Asistente para perfiles.
  
Puede descargar este ejemplo de ejemplos de código de la API de mensajería [de Outlook (MAPI).](https://go.microsoft.com/fwlink/?LinkId=129740
)
  
|||
|:-----|:-----|
|Ejecutable:  <br/> |SABP32.dll  <br/> |
| Directorio de código fuente:  <br/> |SampleAddressBookProvider\SABP  <br/> |
|Idioma:  <br/> |C++  <br/> |
|Plataformas:  <br/> |Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Características admitidas

Este ejemplo admite las siguientes características:
  
- Restricciones de tabla. El ejemplo implementa la resolución de coincidencia de prefijo y nombre ambiguo. No implementa el lenguaje de restricción MAPI completo y las restricciones solo se admiten en el nombre para mostrar.
    
- Una tabla de visualización de detalles para los usuarios de mensajería. 
    
- Direcciones de un solo servidor.
    
- Un cuadro de diálogo de búsqueda avanzada.
    
- Una [interfaz IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) Esta interfaz es parcialmente compatible; sus **métodos IMAPIProp** se delegan a la **interfaz IPropData.** Para obtener más información, vea la [interfaz IPropData : IMAPIProp.](ipropdataimapiprop.md) 
    
- Configuración interactiva y mediante programación.
    
## <a name="unsupported-features"></a>Características no compatibles

En este ejemplo no se admiten las siguientes características:
  
- Ordenación.
    
- Listas de distribución.
    
- Crear, eliminar y modificar entradas.
    
- Propiedades con varios valores.
    
- Propiedades con nombre.
    
- Distinguir entre el nombre y los apellidos en los nombres para mostrar.
    
 **Para instalar el proveedor de libreta de direcciones de ejemplo**
  
1. Para descargar el proveedor de libreta de direcciones de ejemplo, consulte [Descargar los ejemplos MAPI de Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Busque la carpeta donde guardó los ejemplos MAPI de Outlook. Haga clic con el botón secundario en la carpeta zip Número de versión **de \< \> OutlookMAPISamples** y haga **clic en Extraer todo**.
    
3. Haga **clic en** Examinar, seleccione la ubicación donde desea guardar el ejemplo y haga clic en **Extraer**.
    
4. Ejecute Visual Studio 2008.
    
5. En Visual Studio 2008, haga clic en Archivo **,** seleccione **Abrir** y, a continuación, haga clic en **Proyecto/Solución.**
    
6. Vaya a la ubicación donde guardó el ejemplo, haga clic en **SABP.vcproj** y, a continuación, haga clic en **Abrir**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. En el **cuadro de diálogo Guardar archivo** como, haga clic en **Guardar**.
    
9. En la carpeta donde guardó el ejemplo, haga clic con el botón secundario en **install.bat** archivo y haga clic **en Ejecutar como administrador.**
    
10. En el cuadro de diálogo **Control de cuentas de usuario**, haga clic en **Continuar**.
    
    > [!NOTE]
    > **Install.bat** copia el archivo .dll en la carpeta de instalación Microsoft Office predeterminada, C:\Archivos de programa\Microsoft Office\Office12\. Si ha instalado productos de Office en una ubicación diferente, haga clic con el botón secundario **enInstall.bat** haga clic en **Editar**. El archivo se abre en el Bloc de notas. Reemplace la ruta de instalación predeterminada por la ruta de instalación que se usa en el equipo. 
  

