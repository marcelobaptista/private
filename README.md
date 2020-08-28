A estrutura de pastas está assim:

└───Office32
		└───Office
    		└───O365_32
        		└───Office
         		   └───Data
                		└───16.0.11328.20368


Dentro do primeiro nível (pasta raiz Office32) temos 2 arquivos atalho:


Instalar_com_access.lnk

no campo local de destino: tem o caminho \\SERVIDOR\Office\Office32\Office\setup.exe /configure \\SERVIDOR\Office\Office32\Office\config_access.xml
no campo iniciar em: tem o caminho \\SERVIDOR\Office\Office32\Office

Instalar_sem_access.lnk

no campo local de destino: tem o caminho \\SERVIDOR\Office\Office32\Office\setup.exe /configure \\SERVIDOR\Office\Office32\Office\config.xml
no campo iniciar em: tem o caminho \\SERVIDOR\Office\Office32\Office


Conteúdo do config.xml:

 <Configuration ID="80e14e5a-d9e7-4117-874a-e5de9d45555c">
  <Add OfficeClientEdition="32" Channel="Monthly" SourcePath="\\SERVIDOR\Office\Office32\Office\O365_32" ForceUpgrade="TRUE">
    <Product ID="O365ProPlusRetail">
      <Language ID="pt-br" />
      <ExcludeApp ID="Groove" />
      <ExcludeApp ID="Access" /> 
    </Product>
  </Add>
  <Property Name="PinIconsToTaskbar" Value="FALSE" />
  <Property Name="SCLCacheOverride" Value="0" />
  <Property Name="AUTOACTIVATE" Value="FALSE" />
  <Updates Enabled="TRUE" />
  <RemoveMSI />
  <Display Level="Full" AcceptEULA="TRUE" />
  <Logging Level="Off" />
</Configuration>

Conteúdo do config_access.xml:

<Configuration ID="80e14e5a-d9e7-4117-874a-e5de9d45555c">
  <Add OfficeClientEdition="32" Channel="Monthly" SourcePath="\\SERVIDOR\Office\Office32\Office\O365_32" ForceUpgrade="TRUE">
    <Product ID="O365ProPlusRetail">
      <Language ID="pt-br" />
      <ExcludeApp ID="Groove" />
    </Product>
  </Add>
  <Property Name="PinIconsToTaskbar" Value="FALSE" />
  <Property Name="SCLCacheOverride" Value="0" />
  <Property Name="AUTOACTIVATE" Value="FALSE" />
  <Updates Enabled="TRUE" />
  <RemoveMSI />
  <Display Level="Full" AcceptEULA="TRUE" />
  <Logging Level="Off" />
</Configuration>
