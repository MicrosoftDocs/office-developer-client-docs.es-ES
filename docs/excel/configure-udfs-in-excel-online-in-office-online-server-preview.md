---
title: Configurar las UDF en Excel en línea en Office Online Server Preview
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Utilizar funciones definidas por el usuario (UDF) de Excel en línea en Office Online Server Preview para llamar a funciones personalizadas.
ms.openlocfilehash: 2b76b7351a0882762165e37b55c8fbe78f657c34
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384825"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server-preview"></a>Configurar las UDF en Excel en línea en Office Online Server Preview

[Este tema es documentación preliminar y está sujeta a cambios en versiones futuras.] Utilizar funciones definidas por el usuario (UDF) de Excel en línea en Office Online Server Preview para llamar a funciones personalizadas. 
  
Funciones definidas por el usuario (UDF) de Excel Online permiten llamar a funciones personalizadas escritas en código administrado mediante el uso de las fórmulas en las celdas. Puede usar las UDF para:
  
- Call custom mathematical functions.
    
- Get data from custom data sources into worksheets.
    
- Llamar a servicios web.
    
Puede instalar los archivos binarios UDF en una de estas dos ubicaciones:
  
- Un directorio local. Por ejemplo: 
    
    C:\UDFs\MySampleUdf.dll 
    
- La caché de ensamblados global. Por ejemplo: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Hacer referencia a la ubicación cuando se crea una definición de **New-OfficeWebAppsExcelUserDefinedFunction** en Office Online Server Preview. 
  
> [!NOTE]
> Office Online Server Preview no es compatible con UDF que se encuentra en recursos compartidos de red. 
  
## <a name="enable-udfs-on-office-online-server-preview"></a>Habilitar las UDF en Office Online Server Preview

Cuando un administrador crea una nueva granja de servidores de Office Web Apps Server mediante el cmdlet [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell, los ensamblados de UDF están deshabilitados de forma predeterminada. El valor predeterminado de la marca de **ExcelUdfsAllowed** es false. 
  
Para habilitar las UDF, ejecute el siguiente comando de Windows PowerShell en Office Online Server Preview, después de haber creado la granja de servidores de Office Web Apps Server.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server-preview"></a>Crear definiciones de las UDF en Office Online Server Preview

Después de habilitar las UDF, debe crear una definición para el archivo binario que contiene las UDF. Para crear una definición para su UDF binario en Office Online Server Preview, use el cmdlet **New-OfficeWebAppsExcelUserDefinedFunction** . Este cmdlet incluye los siguientes parámetros: 
  
- **Ensamblado**
    
- **UbicaciónDeEnsamblado**
    
- **Habilitar** (se establece en False de forma predeterminada) 
    
- **Descripción**
    
Los siguientes ejemplos muestran cómo crear las definiciones de UDF.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Después de crear la nueva referencia UDF, ejecute **iisreset** en el servidor para seleccionar la referencia inmediatamente. 
  
## <a name="additional-office-online-server-preview-udf-windows-powershell-commands"></a>Comandos adicionales de Office Online Server Preview UDF Windows PowerShell

Use los siguientes cmdlets de Windows PowerShell para trabajar con las UDF:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (sin parámetros obligatorios) - devuelve una lista de definiciones de UDF que se han configurado en Office Online Server Preview. 
    
- **Set-OfficeWebAppsExcelUserDefinedFunction** (El parámetro identity requiere) - establece las propiedades en las definiciones de UDF existentes. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (El parámetro identity requiere) - quita las definiciones de UDF existentes. 
    
## <a name="udf-sample"></a>Ejemplo UDF

Los siguientes archivos proporcionan un libro de ejemplo que usa una UDF y el archivo UDF binario:
  
- [BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx) --un libro de ejemplo que usa una UDF  
- [EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll) --el archivo binario UDF 
    
## <a name="see-also"></a>Vea también

- [Configurar las opciones administrativas Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

