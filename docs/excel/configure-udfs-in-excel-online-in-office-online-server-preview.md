---
title: Configurar las UDF en Excel online en Office Online Server
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Use funciones definidas por el usuario (UDF) en Excel online en Office Online Server para llamar a funciones personalizadas.
ms.openlocfilehash: dbba60a62a1a4783b47c3f1fe40a118dd8ed0d6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311063"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Configurar las UDF en Excel online en Office Online Server

Use funciones definidas por el usuario (UDF) en Excel online en Office Online Server para llamar a funciones personalizadas. 
  
Las funciones definidas por el usuario (UDF) en Excel online permiten llamar a funciones personalizadas escritas en código administrado mediante fórmulas en las celdas. Puede usar las UDF para:
  
- Call custom mathematical functions.
    
- Get data from custom data sources into worksheets.
    
- Llamar a servicios Web.
    
Puede instalar archivos binarios de UDF en una de estas dos ubicaciones:
  
- Un directorio local. Por ejemplo: 
    
    C:\UDFs\MySampleUdf.dll
    
- La memoria caché de ensamblados global. Por ejemplo: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Haga referencia a la ubicación cuando cree una definición **New-OfficeWebAppsExcelUserDefinedFunction** en Office Online Server. 
  
> [!NOTE]
> Office Online Server no admite las UDF que se encuentran en recursos compartidos de red. 
  
## <a name="enable-udfs-on-office-online-server"></a>Habilitar UDF en Office Online Server 

Cuando un administrador crea una nueva granja de servidores de Office Web Apps Server mediante el cmdlet de Windows PowerShell [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) , los ensamblados UDF están deshabilitados de forma predeterminada. El valor predeterminado de la marca **ExcelUdfsAllowed** es false. 
  
Para habilitar las UDF, ejecute el siguiente comando de Windows PowerShell en Office Online Server, una vez creada la granja de Office Web Apps Server.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Crear definiciones de UDF en Office Online Server

Después de habilitar las UDF, debe crear una definición para el binario que contiene las UDF. Para crear una definición para el binario de UDF en Office Online Server, use el cmdlet **New-OfficeWebAppsExcelUserDefinedFunction** . Este cmdlet incluye los siguientes parámetros: 
  
- **MyAssembly**
    
- **AssemblyLocation**
    
- **Habilitar** (se establece en false de forma predeterminada) 
    
- **Descripción**
    
Los ejemplos siguientes muestran cómo crear las definiciones de UDF.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Después de crear la nueva referencia de UDF, ejecute **iisreset** en el servidor para retomar la referencia inmediatamente. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Otros comandos de Windows PowerShell de UDF de Office Online Server

Use los siguientes cmdlets de Windows PowerShell para trabajar con UDF:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (ningún parámetro obligatorio): devuelve una lista de las definiciones de UDF que están configuradas en el servidor de Office online. 
    
- **Set-OfficeWebAppsExcelUserDefinedFunction** (Parámetro Identity obligatorio): establece las propiedades de las definiciones UDF existentes. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (Parámetro Identity obligatorio): quita las definiciones UDF existentes. 
    
## <a name="udf-sample"></a>Ejemplo de UDF

Los siguientes archivos proporcionan un libro de ejemplo que usa un archivo UDF y el binario UDF:
  
- [BooleanDataType. xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): un libro de ejemplo que usa un UDF  
- [EcsUdfsCommonSet. dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): el BINARIo UDF 
    
## <a name="see-also"></a>Vea también

- [Configurar las opciones administrativas de Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

